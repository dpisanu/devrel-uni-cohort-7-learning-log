# Documentation Templates

These templates support a separation-of-concerns approach for the DevRel University learning log.

The goal is to make each weekly file answer one clear question:

| File | Purpose |
|---|---|
| `README.md` | Where do I go for this week? |
| `project-brief.md` | What is the current weekly project snapshot and retrospective? |
| `session-notes.md` | What was taught or discussed in the session? |
| `activities.md` | How did I work through the exercises? |
| `homework.md` | What was asked? |
| `my-submission.md` | What did I answer or create? |
| `public-reflection.md` | What changed in my thinking? |
| `private-resources.md` | What private cohort material exists without republishing it? |
| `public-posts/week-XX-post.md` | What did I share publicly? |

## Template locations

```text
templates/
├── README.md
├── public-posts/
│   └── public-post-template.md
└── sessions/
    ├── activities-template.md
    ├── homework-template.md
    ├── my-submission-template.md
    ├── private-resources-template.md
    ├── project-brief-template.md
    ├── reflection-template.md
    ├── session-notes-template.md
    └── week-template.md
```

## Usage

For each new week, copy the templates from `templates/sessions/` into the relevant `weeks/week-XX-.../` folder and rename them to the target filenames.

For the public post, copy `templates/public-posts/public-post-template.md` into `public-posts/week-XX-post.md`.

## Duplication rule

When the same idea appears in multiple files, choose one source of truth and link to it from the others.

- Full project/personal context belongs in `my-submission.md`.
- The current project snapshot belongs in `project-brief.md`.
- The short weekly summary belongs in `README.md`.
- Learning synthesis belongs in `public-reflection.md`.
- Published social copy belongs in `public-posts/week-XX-post.md`.
