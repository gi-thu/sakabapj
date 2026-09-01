# `docker/setup-buildx-action@v3` — declared runtime evidence

**Observed:** 2026-09-02

| Field | Evidence |
|---|---|
| Action reference | `docker/setup-buildx-action@v3` |
| Resolved commit observed for `v3` | `8d2750c68a42422c14e847fe6c8ac0403b4cbd6f` |
| Declared runtime | **`node20`** |
| Directly affected by GitHub's Node 20 runner removal? | **Yes, at the observed commit** |

## Primary source

Immutable `action.yml` at the observed commit:

https://github.com/docker/setup-buildx-action/blob/8d2750c68a42422c14e847fe6c8ac0403b4cbd6f/action.yml

Relevant declaration:

```yaml
runs:
  using: node20
```

GitHub migration notice:

https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/

## Narrow interpretation

At the commit to which `v3` resolved when inspected on 2026-09-02, this Action explicitly declares the Node 20 JavaScript Action runtime. GitHub's notice says Node 20 is scheduled to be removed from the Actions runner on 2026-09-23.

This card does **not** claim that every workflow using setup-buildx-action v3 will fail, nor does it rate security or general compatibility. The major tag is mutable; this evidence is intentionally tied to the resolved commit above.
