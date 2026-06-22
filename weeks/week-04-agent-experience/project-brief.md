# Project Brief: Week 04

## Project status

**Project name this week:** PlainTrack  
**Previous direction:** Open Source Readiness Field Guide had been shelved as an independent capstone project  
**Current status:** Active capstone project  
**Weekly status:** Public project introduction, problem framing and agent-readiness reflection

## One-sentence project update

This week, **PlainTrack** moved from a resurfaced utility idea into the active capstone project: a developer-native work-time documentation tool built around plain text input, scoped validation rules, deterministic processing, Git traceability and readable reports.

## What changed this week

After shelving the original capstone project, I picked up an older idea that had been sitting in the backlog: making work-time documentation less disconnected from the way technical work actually happens.

The initial trigger was practical. I had needed to create a work-time report during a compliance review and felt again how poorly many time-tracking and reporting workflows integrate with developer-adjacent work. The friction was not only the final report. The bigger issue was maintaining a useful trail that still explains what happened weeks later.

PlainTrack is now framed as a small, opinionated tool that explores this space through software-development patterns:

* plain text as the source input,
* scoped configuration for validation rules,
* deterministic CLI processing,
* Git-friendly traceability,
* HTML reports for review.

## Current product framing

PlainTrack is not intended to become a universal time-tracking platform, an approval system, payroll software, or an employee-monitoring tool.

The current project question is narrower:

> What is the simplest useful path from documented work to a readable report?

This makes the project closer to a static-site-generator pattern than to a conventional enterprise time-tracking dashboard: plain files go in, configurable rules validate them, and a readable output is generated from the documented trail.

## Audience hypothesis

The immediate audience hypothesis is a reachable group of roughly 1,000 possible users, with about 300 potential strong early adopters in my current work environment.

More generally, PlainTrack may fit people who:

* are developers or developer-adjacent professionals,
* already work with files, Git and command-line tools,
* want local-first work-hour records,
* prefer transparent plain-text workflows over opaque time-tracking platforms,
* need reports but dislike reconstructing context from scattered systems later.

## Problem statement

People who need to document work time often have to choose between heavy time-tracking systems, fragile spreadsheets, or informal manual notes. None of these fit particularly well for technical users who want local control, Git-based traceability, transparent rules and reproducible reports.

PlainTrack explores whether work documentation can stay close enough to the work itself that the final report becomes easier to produce later.

## What I worked on this week

This week I shaped PlainTrack from a rough utility idea into a clearer open-source project direction.

The practical work included:

* reviewing the existing tool idea and moving it toward the new PlainTrack framing,
* restructuring code that had grown through a mix of German and English input/output patterns,
* cleaning up consistency bugs introduced during earlier slow evolution stages,
* continuously checking documentation against implementation through AI-assisted Q&A,
* publicly introducing the project through a sequence of LinkedIn posts,
* inviting feedback on work-time documentation workflows and pain points.

## Connection to the Week 04 session

The session introduced a useful new lens: if developers increasingly build with agents, a developer-facing project also needs to ask how agents would interact with it.

For PlainTrack, my working answer is:

> AI agents should interact around PlainTrack, not replace PlainTrack's deterministic core.

This means that agents may help with work-slip creation, missing-entry review, consistency checking, configuration setup and report interpretation. The core validation and processing path should stay deterministic, inspectable and reproducible.

## Agent-readiness implications

The session raised several architectural questions for PlainTrack:

* Does a manual or semi-automated time-reporting workflow still make sense if tools increasingly have access to work-context data?
* Where should manual triggers remain because the user must still own the record?
* Should PlainTrack expose more programmatic interaction points for agents?
* Should output formats be separated more clearly, for example human-readable HTML versus machine-readable JSON?
* Which files, rules, and configuration areas should an agent be allowed to edit?

These questions point toward a future re-architecture that separates data processing, validation, reporting and agent-facing integration more cleanly.

## Decisions made

I decided to:

* release the project publicly,
* speak about the project in public,
* share the idea and invite feedback,
* use the homework as a build-in-public forcing function,
* keep the initial version intentionally small and opinionated.

## Decisions postponed

The following decisions remain open:

* whether and when to release version `0.1`,
* how much of the current workflow and API should be broken during re-architecture,
* what good taste means for PlainTrack's design and implementation,
* how to separate operational concerns inside the tool,
* how to make PlainTrack agent-friendly without weakening its deterministic core.

## Blockers and risks

There are no hard blockers this week, but several risks became visible:

* The project still needs feedback beyond my current work-related filter bubble.
* The public feedback loop did not produce meaningful responses yet.
* The compliance-related context must remain carefully scoped so the project does not become something it should not be.
* Adding options too early could turn a focused workflow into another tool with too much configuration friction.
* Agent-readiness could become a distraction unless it is tied to concrete interaction points.

## Retrospective

### What worked

Switching into a product-shaped capstone project increased my motivation. PlainTrack feels more concrete, smaller and easier to explain than the previous project direction.

The build-in-public activity also forced me to articulate the project more clearly: first as a personal itch, then as a distinction between documentation and measurement, then as a question about whether documentation can survive busy workdays.

### What felt difficult

Publishing the thought process publicly was uncomfortable. I am not naturally strong at public reflection, and the process left me feeling exposed.

It was also difficult to maintain a coherent narrative across a week of posts because the project framing matured from day to day. The plan had to keep changing while the public story was already in motion.

### What felt disappointing

The most difficult moment was not receiving meaningful feedback to the posts. Looking at the stats, the posts mostly reached my work-related filter bubble and did not seem to travel into a broader target audience.

### What I would change next week

Next week I want to:

* release version `0.1`,
* start documenting change ideas through GitHub instead of only through pull requests,
* work more intentionally on showing taste in design and implementation,
* validate whether PlainTrack matters to users beyond my immediate context.
