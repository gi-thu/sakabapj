# GitHub Actions Node 20 / Node 24 Runtime Evidence

**Evidence snapshot: 2026-09-02**

Which GitHub Action refs still explicitly declare `node20` before GitHub removes Node 20 from GitHub Actions runners on **2026-09-23**?

This repository answers one narrow question only: **what runtime is explicitly declared by the exact Action ref's `action.yml` at the source commit observed on 2026-09-02?**

It does **not** rate security, project health, or general compatibility. If the source does not support a conclusion, the answer should be `Unknown` rather than guessed.

GitHub's migration notice says Node 20 will be removed from the Actions runner on 2026-09-23 and asks Action users to update workflows to versions that run on Node 24:

- https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/

## Evidence cards

| Action ref | Declared runtime | Directly affected by Node 20 runner removal? | Evidence |
|---|---:|---:|---|
| `actions/checkout@v4` | `node20` | Yes | [source-linked card](actions-checkout-v4.md) |
| `actions/checkout@v5` | `node24` | No, based on declared runtime | [source-linked card](actions-checkout-v5.md) |
| `actions/setup-node@v4` | `node20` | Yes | [source-linked card](actions-setup-node-v4.md) |
| `actions/setup-node@v5` | `node24` | No, based on declared runtime | [source-linked card](actions-setup-node-v5.md) |
| `actions/cache@v4` | `node20` | Yes | [source-linked card](actions-cache-v4.md) |
| `actions/upload-artifact@v4` | `node20` | Yes | [source-linked card](actions-upload-artifact-v4.md) |
| `github/codeql-action/init@v3` | `node20` | Yes | [source-linked card](github-codeql-action-init-v3.md) |
| `docker/setup-buildx-action@v3` | `node20` | Yes | [source-linked card](docker-setup-buildx-action-v3.md) |

## How to read this

Major tags such as `v4` can move. Each card therefore records both the human-facing ref and the **resolved commit SHA observed on 2026-09-02**, and links to the immutable source at that commit.

`Directly affected = Yes` means only this: the inspected Action source explicitly declares `runs.using: node20`, while GitHub's migration notice says the runner's Node 20 runtime is scheduled for removal. It is not a claim that a workflow is otherwise broken, unsafe, or incompatible.

## Why this tiny repository exists

This is a deliberately small public experiment. Before building a scanner, API, dashboard, database, or large directory, the question is whether unknown users discover and use source-linked runtime evidence at all.
