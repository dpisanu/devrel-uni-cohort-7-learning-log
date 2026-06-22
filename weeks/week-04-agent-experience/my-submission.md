# My Submission: Week 04

## Submission overview

This submission covers the three Week 04 homework areas:

1. a project article / project explanation for PlainTrack,
2. public build-in-public posts,
3. AI-agent research and reflection.

The active capstone project is **PlainTrack**.

---

## Part 1: Small article about the project

# PlainTrack: keeping work-time documentation close to the work

PlainTrack is a developer-native work-time documentation tool.

The project started from a personal friction point: documenting working time often happens after the fact, in tools that are disconnected from the actual work. Meetings, deployments, bug investigations, customer conversations and documentation work leave traces across many systems, but the final report often reduces the day to a few numbers and rough categories.

PlainTrack explores a smaller question:

> Can work documentation stay close enough to the work itself that the final report becomes easier to produce later?

## What I am building

PlainTrack is currently shaped around a simple workflow:

1. Write work records in plain text.
2. Validate them with configurable rules.
3. Generate readable reports from the documented trail.

The tool is intentionally small and opinionated. It uses patterns that feel natural in developer-adjacent workflows:

* files as the source of truth,
* Git for history and traceability,
* a command-line tool for validation and report generation,
* readable HTML output for review,
* scoped configuration instead of a large platform.

The mental model is closer to a static site generator than to a classic time-tracking dashboard: plain content goes in, rules process it, and a publishable report comes out.

## Who it is for

The first audience is developers and developer-adjacent professionals who already spend much of their workday in files, tickets, commits, terminals and documentation.

These users may need to document working time but prefer:

* local-first records,
* transparent data,
* reproducible reports,
* Git-based traceability,
* simple plain-text workflows,
* fewer context switches into separate reporting tools.

The immediate test audience may be people in my own work environment who face similar reporting friction.

## What problem it solves

Many work-time tools focus on measurement: hours, totals, allocation, balances and reports.

Those numbers matter, but they often do not explain the work.

A report may say that I spent eight hours on a day. It may not explain which deployment caused follow-up work, which customer conversation changed priorities, or which documentation effort unblocked the next step.

PlainTrack is interested in the relationship between documentation and measurement:

* documentation gives context,
* measurement gives totals,
* reports become more meaningful when the trail is still available.

Without documentation, measurement becomes a spreadsheet. Without measurement, documentation becomes a diary. PlainTrack tries to connect the two without creating a heavy workflow.

## Why this project matters

When work gets busy, documentation is often one of the first things to degrade.

What remains is often a rough reconstruction: part time entry, part estimate, part memory. I started calling this a **time'stimate**.

This is understandable. Busy people do not intentionally keep bad records. The workflow often fails because documentation is too far away from the work itself.

PlainTrack matters if it can make the documentation step small enough that it survives busy workdays.

## How someone can interact with it

At the current stage, someone can interact with the project by:

* reading the public project posts,
* reviewing the repository once shared,
* trying the current version,
* giving feedback on the workflow,
* comparing it to their own work-time documentation process,
* challenging the assumptions behind the input format, validation rules and reports.

The most useful feedback at this stage is not feature requests. It is friction mapping:

* What do people currently use?
* Where does that workflow break?
* What do they document versus estimate afterwards?
* Does a plain-text workflow feel natural or unrealistic?
* What would make the generated report useful?

## What I learned so far

The biggest lesson so far is that simplicity needs constraints.

It is easy to add more fields, more states, more categories and more options. But if the problem is that documentation breaks under pressure, adding more workflow weight is probably the wrong direction.

PlainTrack needs to protect its core workflow:

> documented work → validation → readable report

The current challenge is deciding which constraints are helpful, which are too limiting and which protect the project from becoming another tool that tries to support every workflow.

## How AI influenced the workflow

AI helped mostly as a review and reflection partner.

I used AI-assisted Q&A to compare documentation against implementation, identify unclear explanations and think through how the tool might behave in an AI-first landscape.

The Week 04 session also made me think differently about agent-readiness. PlainTrack has AI-friendly properties already: flat files, deterministic validation and generated output. But it is not yet designed for agent workflows.

My current position is:

> AI agents should interact around PlainTrack, not replace PlainTrack's deterministic core.

Agents could help draft entries, check consistency, suggest missing context, review configuration and generate summaries. The source of truth should remain inspectable and under user control.

---

## Part 2: Build in public

For Part 2, I created a sequence of public LinkedIn posts around PlainTrack.

| Post | Focus | Link |
| --- | --- | --- |
| Post 1 | Introducing PlainTrack as the new capstone project and framing work documentation as a trail. | <https://www.linkedin.com/posts/daniel-pisanu_devrel-devreluni-developerrelations-activity-7473090147408855043-xJgY> |
| Post 2 | Distinguishing documentation from measurement. | <https://www.linkedin.com/posts/daniel-pisanu_devrel-developerrelation-devreluni-activity-7473502124899954689-IK8w> |
| Post 3 | Introducing the idea of the time'stimate: part entry, part estimate, part reconstruction. | <https://www.linkedin.com/posts/daniel-pisanu_devrel-developerrelations-devreluni-activity-7473864066835537920-Wkat> |
| Post 4 | Explaining why PlainTrack should start small and opinionated. | <https://www.linkedin.com/posts/daniel-pisanu_devrel-developerrelations-devreluni-activity-7474215121679048704-N-aH> |
| Post 5 | Turning the question outward and inviting feedback on work-time documentation workflows. | <https://www.linkedin.com/posts/daniel-pisanu_devrel-developerrelations-devreluni-activity-7474560503756029953-tFXr> |

The post series moved through this narrative:

1. Work leaves a trail.
2. Documentation gives meaning to measurement.
3. Busy days degrade documentation into rough time'stimates.
4. Simplicity requires constraints.
5. The project needs feedback from people who face this problem in their own workflows.

The main unresolved issue is that the posts did not yet produce the feedback loop I hoped for. They mostly reached my existing work-related filter bubble.

---

## Part 3: Researching AI agents

### Activity 1: Trying an agent-like workflow myself

I deployed a local `n8n` container and built an automation pipeline around my work documentation data.

The pipeline:

1. pulls work documentation data from the Git repository,
2. runs a modified version of the PlainTrack/TimeTrack tooling to validate data integrity,
3. runs another modified check that sends a one-line status message if a time threshold suggests that the timeframe may be underbooked.

There was not yet a full AI agent involved. At this point, the toolchain is closer to automation than autonomy.

That distinction matters: PlainTrack currently behaves like a deterministic post-timeframe reporting tool. It does not yet have agent-facing infrastructure.

### What agent(s) did I explore?

I explored three areas:

* **n8n automation** for data integrity checks, report generation and notification workflows.
* **GitHub Copilot** as a possible side-by-side assistant, though the work was not primarily a programming task and therefore felt like overkill.
* **LocalAI** as a possible local-first AI agent direction, but the setup friction slowed me down before I could make meaningful progress.

The local-first angle is important because PlainTrack deals with person-specific work-time data. Any AI-assisted workflow should fit the project’s data-sovereignty tone.

### What are the most interesting or surprising use cases I found?

I found three AI use cases especially surprising:

* sleep optimization through personal and environmental habit tracking,
* counterfeit detection through 3D scans of originals and edge-device comparison,
* sentiment matching to identify production problems before conventional production sensors detect them.

The broader lesson is that agentic or AI-assisted systems become interesting when they combine signals, context and action in workflows that would otherwise be too slow or too fragmented for humans to run continuously.

### What workflows are people automating with agents?

The most visible use cases I currently see are:

* discussion consolidation and information condensation,
* deep research assistance, especially when combined with speech-to-text workflows,
* ticket triage for technical and support teams,
* reducing friction in test and validation stages,
* using autonomous or semi-autonomous agents around TDD, BDD and side-by-side development workflows.

The pattern is that agents are most useful where work is repetitive, context-heavy and reviewable.

### What felt genuinely useful versus mostly hype?

The useful part is targeted automation around specific friction points.

Examples that feel useful:

* checking whether records are complete,
* reviewing documentation drift,
* summarizing discussions,
* creating draft content for review,
* detecting inconsistencies,
* opening a pull request that a human can inspect.

The hype-heavy part is the idea that a mail agent, browser agent, or general-purpose autonomous assistant can simply replace a person across broad digital workflows.

That promise often moves the work instead of removing it. Guardrails need maintenance. Escalation paths need design. Edge cases need review. The owner still has to understand what the agent is doing and when it should not act.

### What limitations or frustrations did I notice?

The tools are impressive, but the limiting factor is often onboarding cost.

For local AI in particular, the software and hardware requirements can be frustrating. I like the Unix principle: one tool does one thing well, and the power comes from chaining tools together. Many AI services currently feel heavier than that. They can be powerful, but the setup and integration cost is not always small.

The other limitation is personal capacity. The tooling landscape is moving quickly, and keeping up requires willingness, expertise, creativity and access.

### What implications could this have for DevRel?

DevRel needs to understand not only how humans use a product, but also how agents interact with the product on behalf of humans.

That creates additional pressure on DevRel and developer experience teams:

* documentation needs to be clear to humans and machines,
* examples need to be runnable and agent-consumable,
* SDKs and CLIs need predictable behavior,
* product surfaces may need skills, MCP servers, or other agent-facing integration points,
* communities may need help understanding what is actually useful versus what is hype.

This also raises the skill bar. DevRel practitioners may need to combine community sense, content skill, product taste, technical depth and agent-workflow literacy.

### What implications could this have for software development?

AI can speed up prototyping, testing and validation. It may reduce sunk-cost pressure because ideas can be explored and discarded faster.

At the same time, software development still needs reproducibility, traceability and predictability. That is not always a natural fit with fast-moving AI systems.

The operator still needs understanding. If AI abstracts too much away, the question becomes what remains on the human side: judgment, architecture, taste, validation, responsibility and context.

### What implications could this have for PlainTrack?

PlainTrack can benefit from AI in several ways:

* prototyping new interaction ideas quickly,
* generating draft documentation,
* reviewing consistency between docs and implementation,
* helping users create draft work slips,
* checking missing records,
* suggesting report improvements.

But PlainTrack should remain deterministic at the core.

The agent-friendly future is not a fully autonomous time tracker. The better direction is a tool with clear contracts:

* input format contract,
* grammar contract,
* language contract,
* machine-readable output contract,
* operational permission contract.

That would allow AI systems to assist while keeping the user in control of the record.

## Final reflection

The goal of the homework was to start building intuition around where software, learning and developer workflows are heading.

For me, that intuition is this:

> Agents are most useful when they reduce friction around a clear workflow, but they should not erase ownership, judgment or the need for understandable systems.

For PlainTrack, that means building a reliable deterministic core first, then designing carefully chosen agent interaction points around it.
