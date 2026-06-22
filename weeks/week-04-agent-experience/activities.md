# Activities: Week 04

## Activity context

The Week 04 activity asked participants to look at their project through the lens of AI agents.

The prompt was:

> Use your favourite AI assistant, feed in information about your project and what you built so far, and then answer questions about where an AI agent could interact with your product, what currently breaks for agents and what you would redesign.

## Activity prompts

1. Could an AI agent interact with your product? If yes, where?
2. What currently breaks for agents?
3. Is there something you would redesign?

## My project context

The active project this week is **PlainTrack**, a CLI-based, developer-native work-time documentation tool.

**PlainTrack** already has a few AI-friendly patterns:

* flat-file based input,
* a validation core based on simple rules,
* deterministic processing,
* generated reports from accumulated information.

The core position I would use for this activity is:

> AI agents should interact around PlainTrack, not replace PlainTrack's deterministic core.

## 1. Could an AI agent interact with PlainTrack? If yes, where?

Yes, but the most useful interaction points are around the toolchain rather than inside the core validation logic.

### Possible interaction point: work-slip creation

An AI assistant could help create draft work slips from context that already exists elsewhere, such as notes, tickets, commits, calendar entries, or short user dictation.

The important boundary is that the user should still review and approve the final work record. PlainTrack should not silently invent or finalize person-specific work-time data.

### Possible interaction point: missing-entry and consistency review

An agent could review a set of PlainTrack files and identify likely issues:

* missing days,
* incomplete entries,
* inconsistent tags,
* suspicious totals,
* records that do not match the configured rules,
* entries that need clarification before a report is generated.

This is a strong fit because the task is repetitive, structured and review-oriented.

### Possible interaction point: configuration setup and review

An agent could help bootstrap or review a project-specific PlainTrack configuration:

* required fields,
* allowed projects,
* expected working-time windows,
* validation thresholds,
* report settings.

Again, this should be assistive. The agent may propose config changes, but the user or project owner should approve them.

## 2. What currently breaks for agents?

I have not yet given an agent a serious end-to-end run against **PlainTrack**, so these are assumptions based on the current shape of the project.

### Human-oriented documentation

The documentation currently explains the grammar for natural operators. That is useful, but agents often need stricter contracts and clearer examples.

Some ambiguity is intentional for natural operators but risky for agent operators.

### Exact grammar markers

**PlainTrack** depends on exact markers and keywords. From experience, AI systems often introduce small variants when writing structured text.

That could break validation even when the output looks close to correct.

### Localization drift

Because the tool previously evolved through a mix of German and English input/output, localization is a risk. An agent with different language settings may produce terms, dates, labels, or phrasing that look natural but do not match the expected grammar.

### Output format mismatch

**PlainTrack** currently produces CLI and HTML-oriented outputs. Those are good for natural operators, but agent operators may need machine-readable outputs such as JSON to reliably inspect validation state, totals, warnings and report metadata.

### Permission ambiguity

It is not yet clear what an agent should be allowed to change.

Examples:

* Can an agent add work slips?
* Can an agent modify existing records?
* Can an agent change validation rules?
* Can an agent regenerate reports?
* Can an agent edit historical entries?

Without an operational contract, agent assistance could easily cross a boundary it should not cross.

## 3. Is there something I would redesign?

Yes. The session made me think that **PlainTrack** needs clearer boundaries between human-facing workflow, machine-facing contracts and deterministic processing.

## Redesign wishlist

### Format contract for input data

**PlainTrack** should document a stricter input contract that is easy for both humans and agents to follow.

This could include:

* required fields
* exact marker syntax
* accepted date/time formats
* allowed optional fields
* examples of valid and invalid entries

### Grammar contract

The tool should define and enforce grammar markers clearly enough that agents do not invent nearby alternatives.

The contract should make it obvious that `project`, `Project`, `Projekt`, and similar variants are not necessarily interchangeable unless explicitly configured.

### Language contract

**PlainTrack** should separate natural-language entry content from operational keywords.

That would make it easier to avoid localization issues while still allowing users to describe work in their own language.

### Output selection

The current workflow produces CLI and HTML output. Future versions should separate output formats more explicitly.

Possible outputs:

* human-readable CLI output
* HTML report output
* JSON validation output
* JSON report data
* machine-readable warning summaries

### Separation of processing and reporting

**PlainTrack** should separate data processing from result generation more cleanly.

That would make it easier for agents and automation systems to call only the part they need:

* validate records
* compute totals
* check consistency
* generate reports
* export machine-readable state

### Operational contract for agents

**PlainTrack** should define what AI systems are allowed to do.

Example policy categories:

| Operation | Possible default |
| --- | --- |
| Read work records | Allowed |
| Suggest new entries | Allowed |
| Create draft entries | Allowed with review |
| Modify existing entries | Review required |
| Change validation rules | Owner approval required |
| Delete historical records | Not allowed by default |
| Generate reports | Allowed |

## What changed or clarified my thinking

The activity clarified that **PlainTrack** should not become an agent that tracks time on behalf of the user.

The stronger direction is to keep **PlainTrack** deterministic and inspectable, while making the surrounding workflow easier for agents and automation systems to support.

## Open questions

* What is the smallest agent-facing contract **PlainTrack** needs for version `0.1`?
* Should machine-readable JSON output be part of the first release or the re-architecture after `0.1`?
* How much ambiguity should remain for natural operator convenience?
* Where should the user be forced to approve generated or modified work records?
* How can the tool support agent workflows without becoming dependent on a specific AI platform?

## Public-safe source boundary

The live Miro board screenshots are treated as private cohort material. The activity prompts are reconstructed here at a high level, and the answers are my own.
