# Contributing

These rules apply to every repository in this organization. A repository can add its own
`CONTRIBUTING.md` for tooling, tests and domain rules; for git it links back here.

Everything is in English: code, comments, commit messages, issues and pull requests. Fixed
values a program reads and text shown in a user interface stay in their original language.

## Issues

Every bug, todo and idea is an issue. An issue says:

- **What** is wrong or wanted
- **Why** it matters
- **Where**: tool, file or module
- **How to reproduce** (bugs)

Labels, kept short:

| Label | Meaning |
|---|---|
| `bug`, `todo`, `idea` | Type |
| `in progress` | Someone is working on it (also assign yourself) |
| `decision` | Needs a decision from the maintainer before work starts |
| `userfeedback` | Reported by a real user of the tools. Never for findings by developers or agents |

Before you start: assign the issue to yourself, add `in progress` and comment with your branch
name. If you find something else on the way, open a new issue instead of fixing it in the same PR.

## Branches

- `main` is reviewed and releasable. **Never commit or push to `main` directly.**
- One branch per issue, with the issue number: `feat/12-short-name`, `fix/14-short-name`
  (`docs/` and `chore/` when they fit).
- Several people, sessions or agents at once: each works in its own branch (and worktree),
  never on someone else's branch.

## Commits

[Conventional Commits](https://www.conventionalcommits.org/) with the issue number:

```text
feat: add room area tool (#12)
fix: correct door width rounding (#14)
refactor: extract shared validation (#15)
docs: describe the release process (#16)
```

Prefixes: `feat:` `fix:` `refactor:` `docs:` `test:` `chore:`.

## Pull requests

- One pull request per issue, against `main`, when the change is ready for review.
- One `Closes #12` line per issue it resolves, so merging closes them. Issues only mentioned
  for context go under `Related:` and stay open.
- Describe how you tested the change.
- The maintainer reviews every pull request before merge. Merge strategy: **squash merge**
  (one commit per issue on `main`).
- Conflicts: the author rebases the branch onto `main` and resolves them.

## Releases

A release is a **tag on `main`**, never on a branch. Each product defines its tag format and
who may set it in its own repository.

## Working with AI agents

- One issue, one agent, one branch.
- Agents push and open pull requests only when a person asks for it, and never merge on their own.
- A commit or pull request made with an agent keeps its `Co-Authored-By` line.
- Anything an agent has not verified is marked as a guess.
