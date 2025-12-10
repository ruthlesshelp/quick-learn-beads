# Quick, learn Beads
_Beads_ is Steve Yegge's lightweight memory system for coding agent.

Learn more:
* https://steve-yegge.medium.com/introducing-beads-a-coding-agent-memory-system-637d7d92514a
* https://steve-yegge.medium.com/beads-best-practices-2db636b9760c

# Installation Quick Start

This is an intentionally abbreviated TL;DR just to illustrate how to get started. For complete instructions, please refer to Steve Yegge's GitHub repository and the [Installation](https://github.com/steveyegge/beads?tab=readme-ov-file#installation) and [Quick Start](https://github.com/steveyegge/beads?tab=readme-ov-file#quick-start) sections.

## Homebrew (macOS/Linux)

```zsh
brew tap steveyegge/beads
brew install bd
```

To confirm things are working ... 

```zsh
bd --version
```

returns something like ...

> bd version 0.29.0 (c9eeecf0)

## Git is a requirement

Make sure your project is a Git project.

Running ... 

```zsh
git status
```

should return something like ...

> On branch main
> Your branch is up to date with 'origin/main'.
> 
> nothing to commit, working tree clean

If NOT, you will need to initialize you project as a Git repository. More info [here](https://kbroman.org/github_tutorial/pages/init.html)

## Minimal Setup

"Beads is designed for AI coding agents to use on your behalf."

You (the human) run the initialization once to get things started.

```zsh
bd init
```

Read about the files created by `bd init` here:
https://github.com/steveyegge/beads?tab=readme-ov-file#files-created-by-bd-init

# Start the Project Work

## Seed the First Task

Okay, let's get started.

You will need to seed Beads with the first task.

```zsh
bd create "Spec from Kata Description" -p 1 -t task
```

## Make the agent use `bd`

Using the VS Code GitHub Copilot agent mode, describe what you want you want the Copilot agent to do.

> You are working in a repository that uses Beads via the bd CLI for task and dependency tracking.
> - When proposing plans, create/update issues with bd create, bd edit, bd dep add, and show bd list before doing work.
> - Use bd close for done items and keep dependencies accurate.
> - Prefer bd dep tree <id> to decide the next unblocked item.

## Explain the First Task

Explain to the Copilot agent what the first task is all about.

> Now that the workspace is set up with Beads, I would like to first explain the "Spec from Kata Description" task before you get started.
> 
> You are my spec engineer.
> 
> We’ll convert the Kata Description `docs/KATA_DESCRIPTION.md` into a formal specification for spec‑driven development.
> 
> Save the spec in a separate `docs/SPEC.md` file.
> 
> The spec must be unambiguous, testable, and organized to match widely-adopted product requirements document (PRD) and software engineering practices.
> 
> Maintain requirement IDs and cross‑references for traceability. If things are ambiguous, list concrete clarification questions in a separate `docs/CLARIFICATION_QUESTIONS.md`.

## Tackle The Next Priority Task

Explain to the Copilot agent that it should _tackles the next priority task_.

> tackle the next priority task
