# `actions/upload-artifact@v4` — declared runtime evidence

**Observed:** 2026-09-02

| Field | Evidence |
|---|---|
| Action reference | `actions/upload-artifact@v4` |
| Resolved commit observed for `v4` | `ea165f8d65b6e75b540449e92b4886f43607fa02` |
| Declared runtime | **`node20`** |
| Directly affected by GitHub's Node 20 runner removal? | **Yes, at the observed commit** |

## Primary source

Immutable `action.yml` at the observed commit:

https://github.com/actions/upload-artifact/blob/ea165f8d65b6e75b540449e92b4886f43607fa02/action.yml

Relevant declaration:

```yaml
runs:
  using: node20
```

GitHub migration notice:

https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/

## Narrow interpretation

At the commit to which `v4` resolved when inspected on 2026-09-02, this Action explicitly declares the Node 20 JavaScript Action runtime. GitHub's notice says Node 20 is scheduled to be removed from the Actions runner on 2026-09-23.

This card does **not** claim that every workflow using upload-artifact v4 will fail, nor does it rate security or general compatibility. The major tag is mutable; this evidence is intentionally tied to the resolved commit above.
