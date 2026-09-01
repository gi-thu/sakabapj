# `actions/checkout@v5` — declared runtime evidence

**Observed:** 2026-09-02

| Field | Evidence |
|---|---|
| Action reference | `actions/checkout@v5` |
| Resolved commit observed for `v5` | `fbc6f3992d24b796d5a048ff273f7fcc4a7b6c09` |
| Declared runtime | **`node24`** |
| Directly affected by GitHub's Node 20 runner removal? | **No, based on the observed runtime declaration** |

## Primary source

Immutable `action.yml` at the observed commit:

https://github.com/actions/checkout/blob/fbc6f3992d24b796d5a048ff273f7fcc4a7b6c09/action.yml

Relevant declaration:

```yaml
runs:
  using: node24
```

GitHub migration notice:

https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/

## Narrow interpretation

At the commit to which `v5` resolved when inspected on 2026-09-02, this Action explicitly declares the Node 24 JavaScript Action runtime. Therefore the specific Node 20 runtime-removal condition described in GitHub's notice does not apply to this observed declaration.

This does **not** claim universal workflow or operating-system compatibility. The major tag is mutable; this evidence is intentionally tied to the resolved commit above.
