# Contributing to the hardware library

---

## Before you start

- Check that the component you are adding does not already exist under a different name.
- Check that the MPN (Manufacturer Part Number) is correct and the component is available.
- All PRs require at least one review before merge. See [CODEOWNERS](.github/CODEOWNERS).

---

## Commit message format

Use [Conventional Commits](https://www.conventionalcommits.org/):

| Change | Commit format |
|---|---|
| New component | `feat(symbols): add TI_OPA2134 op-amp symbol` |
| Correction | `fix(footprints): correct pad spacing on SOIC-8` |
| New SPICE model | `feat(spice-models): add TI_OPA2134 SPICE model` |
| Reorganisation | `refactor(footprints): move SOT-23 variants to SOT-23.pretty` |
| Breaking change | `feat!(symbols): rename OPA2134 to TI_OPA2134` |

Breaking changes (`!`) affect any feature that uses the changed component. Note in the PR description which features may be affected.

---

## Adding a new component

1. Create a branch: `library/<type>/<description>` — e.g. `library/symbol/TI-OPA2134`
2. Add the symbol, footprint, 3D model, and SPICE model as applicable
3. Work through the [component addition checklist](checklists/component-addition.md) — tick every item
4. Open a PR with a `feat:` commit message
5. Request review from CODEOWNERS
6. Do not merge without at least one approval

---

## Updating an existing component

1. Create a branch: `library/fix/<description>` — e.g. `library/fix/soic8-pad-spacing`
2. Work through the [component update checklist](checklists/component-update.md) — tick every item
3. Open a PR with a `fix:` commit message (or `feat!:` if it is a breaking change)
4. If it is a breaking change, note in the PR description which feature repositories use the affected component

---

## Releases

Release tags are created periodically by merging the release-please Release PR. You do not need to create tags manually. Add your changes with conventional commits and they will appear in the next release changelog automatically.
