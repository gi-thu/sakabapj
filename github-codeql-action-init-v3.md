# `github/codeql-action/init@v3` — declared runtime evidence

**Observed:** 2026-09-02

| Field | Evidence |
|---|---|
| Action reference | `github/codeql-action/init@v3` |
| Resolved commit observed for `v3` | `6f5948dfacef28e207b48d0905cf90c03365536d` |
| Declared runtime | **`node20`** |
| Directly affected by GitHub's Node 20 runner removal? | **Yes, at the observed commit** |

## Primary source

Immutable `init/action.yml` at the observed commit:

https://github.com/github/codeql-action/blob/6f5948dfacef28e207b48d0905cf90c03365536d/init/action.yml

Relevant declaration:

```yaml
runs:
  using: node20
```

GitHub migration notice:

https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/

## Narrow interpretation

At the commit to which `v3` resolved when inspected on 2026-09-02, the `init` Action explicitly declares the Node 20 JavaScript Action runtime. GitHub's notice says Node 20 is scheduled to be removed from the Actions runner on 2026-09-23.

This card intentionally targets `github/codeql-action/init@v3`. The repository-root `github/codeql-action@v3` action is a composite stub and is not treated as the same Action reference. This card does **not** rate CodeQL security, workflow correctness, or general compatibility.
