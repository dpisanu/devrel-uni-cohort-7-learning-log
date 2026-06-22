# Session Notes: From Developer Experience to Agent Experience

## Session metadata

**Session:** From Developer Experience to Agent Experience  
**Date:** 19.05.2026  
**Speaker:** Hassan El Mghari  
**Role:** Director of Developer Experience at Together AI  
**Social links:** [LinkedIn](https://www.linkedin.com/in/nutlope/) · [GitHub](https://github.com/Nutlope) · [Website](https://www.nutlope.com/) · [X](https://x.com/nutlope)

## One-sentence summary

Developer experience is expanding toward agent experience: DevRel still serves humans, but developer-facing products increasingly need to be understandable, usable and valuable in workflows where humans build together with AI agents.

## Theme

The official session theme focused on what changes when AI agents are no longer only assisting developers but actively participating in how software is built.

My framing of the theme:

> The session connected DevRel craft, public building, product taste and agent-ready workflows. It challenged me to ask not only what my project does for users, but also how it behaves in a world where users increasingly work through AI-assisted tooling.

## Key takeaways

### 1. DevRel spans community, content and product

The session framed DevRel through three overlapping areas:

| Area | Typical focus |
| --- | --- |
| Community | Events, livestreams, Discord/Slack communities and relationship-building. |
| Content | Blog posts, videos, courses, talks and educational material. |
| Product / DX | Code samples, example apps, documentation, SDKs, CLIs and platform feedback. |

This was useful because it made the breadth of DevRel more explicit. The role is not one activity. It sits across building, explaining, teaching, connecting and improving the developer experience.

### 2. Good taste matters more when building becomes faster

AI lowers the effort required to produce code, content and prototypes. That makes taste more important, not less important.

In this context, taste means more than visual polish. It includes:

* choosing a clear problem,
* making the result feel intentional,
* adding a human point of view,
* designing a simple and coherent experience,
* knowing when not to add more features,
* producing work that feels useful rather than generic.

For PlainTrack, this connects directly to the question of simplicity. The project should not become a configurable option jungle. It should protect the smallest useful workflow.

### 3. Agent Experience is becoming part of Developer Experience

Agent Experience asks whether an AI agent can successfully understand and use a product, not only whether a human developer can.

The session pointed toward several agent-facing surfaces:

* documentation that agents can consume reliably,
* SDKs and CLIs that agents can call or reason about,
* skills or reusable instruction bundles,
* MCP-style integrations,
* examples that make product usage obvious,
* workflows where agents can safely open pull requests or suggest changes.

For PlainTrack, this reframes the project from “Can a developer use this CLI?” to “Can a developer and their tools safely work around this CLI without corrupting the source of truth?”

### 4. Build simple things well and ship visibly

A recurring theme was the value of simple, focused applications that do one thing well. A project does not have to be completely unique to be useful. It needs to be clear, well-built, easy to understand and easy to try.

This connects strongly to PlainTrack. The project should stay easy to describe:

> Plain text work records in, validated readable reports out.

The week’s public posts were also a reminder that shipping visibly is its own skill. Building in public is not just publishing a link. It requires framing the problem, giving people a reason to care, and asking questions that invite a response.

### 5. AI workflows can support DevRel operations

The session included practical examples of AI-assisted workflows around documentation, internal tooling and automation. The important pattern was not “automate everything.” The more useful pattern was:

1. identify where a workflow repeatedly falls out of date or creates friction,
2. automate the check or reminder,
3. keep humans involved for decisions and quality judgment,
4. use agents to reduce manual overhead where the task is repeatable.

This is relevant to PlainTrack because the tool itself is about reducing reporting friction without removing human ownership of the work record.

## Concepts and models introduced

### Three-area DevRel map

The session’s DevRel map helped separate community, content and product work. This is useful for understanding why DevRel roles can look so different across organizations.

For my own project, this also creates a useful checklist:

* **Product:** Is PlainTrack useful and coherent?
* **Content:** Can I explain the problem and workflow clearly?
* **Community:** Can I find people who recognize the friction and are willing to respond?

### Good taste

Good taste was presented as a practical hiring and building signal. It shows up in the quality of artifacts, examples, content, demos and design choices.

For PlainTrack, good taste may mean:

* opinionated defaults,
* clean plain-text patterns,
* a minimal rule system,
* readable reports,
* careful boundaries around what the tool refuses to become.

### Agent Experience

Agent Experience is the shift from only optimizing for human developers toward also optimizing for AI-assisted workflows.

For PlainTrack, Agent Experience may require:

* a stricter input contract,
* a grammar contract to avoid keyword variants,
* a language contract to avoid localization drift,
* machine-readable output such as JSON,
* explicit operational permissions for what agents may and may not change.

### Builder backlog and timing

The session emphasized keeping a backlog of ideas and revisiting them as technology changes. Old ideas can become newly viable when model capabilities, tooling, or user expectations shift.

PlainTrack is an example of this pattern. The idea had existed before, but the current DevRel University context and AI-agent discussion gave it a new frame.

## Q&A themes that extended the keynote

The Q&A expanded the keynote into practical DevRel operations:

* keeping documentation up to date through targeted automation,
* using GitHub Actions or similar automation where repeated drift occurs,
* evaluating skills and agent-facing workflows through concrete tasks,
* using example apps to discover product friction,
* sharing useful work repeatedly to build audience over time.

The most relevant Q&A idea for my project was that automation should start where drift or friction is visible. For PlainTrack, this points to missing-entry checks, validation, consistency review and report generation rather than full autonomy.

## My interpretation

The session made the new capstone project feel both more promising and more demanding.

PlainTrack has several agent-friendly qualities already: flat files, validation logic, deterministic output and report generation. But it is not yet designed as an agent-ready product. The current documentation is still written mainly for human controllers. The input grammar leaves intentional ambiguity. The output is primarily human-readable.

The useful conclusion is not to make PlainTrack an AI product. The useful conclusion is to design stronger boundaries so AI tools can support the workflow around it.

## Public-safe source boundary

These notes are based on my own session notes, public-safe slide screenshots and a high-level synthesis of private cohort material. Screenshots, transcripts, Miro board content and cohort-only details are not republished here.
