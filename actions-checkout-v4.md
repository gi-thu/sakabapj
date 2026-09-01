# `actions/checkout@v4` — declared runtime evidence

**Observed:** 2026-09-02

| Field | Evidence |
|---|---|
| Action reference | `actions/checkout@v4` |
| Resolved commit observed for `v4` | `11d5960a326750d5838078e36cf38b85af677262` |
| Declared runtime | **`node20`** |
| Directly affected by GitHub's Node 20 runner removal? | **Yes, at the observed commit** |

## Primary source

Immutable `action.yml` at the observed commit:

https://github.com/actions/checkout/blob/11d5960a326750d5838078e36cf38b85af677262/action.yml

Relevant declaration:

```yaml
runs:
  using: node20
```

GitHub migration notice:

https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/

## Narrow interpretation

At the commit to which `v4` resolved when inspected on 2026-09-02, this Action explicitly declares the Node 20 JavaScript Action runtime. GitHub's notice says Node 20 is scheduled to be removed from the Actions runner on 2026-09-23.

This card does **not** claim that every workflow using checkout v4 will fail, nor does it rate security or general compatibility. The major tag is mutable; this evidence is intentionally tied to the resolved commit above.
