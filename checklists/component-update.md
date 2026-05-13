# Component Update Checklist

> Work through this checklist when raising a PR to correct or update an existing component.
> Tick every item. For breaking changes, complete the additional section below.

## Change scope

- [ ] Change description is clear in the PR description and commit message
- [ ] Commit type is correct: `fix:` for corrections, `feat!:` or `fix!:` for breaking changes

## Verification

- [ ] Updated symbol passes KiCad ERC with zero errors
- [ ] Updated footprint dimensions verified against datasheet
- [ ] If pad numbering changed: symbol pin numbering updated to match
- [ ] If 3D model changed: alignment re-verified in KiCad 3D viewer
- [ ] If SPICE model changed: model re-tested in minimal simulation

## Breaking changes (complete only if this is a breaking change)

A breaking change is any of:
- Symbol or footprint renamed
- Pad numbering or pad dimensions changed on existing footprint
- Component removed

- [ ] PR description notes that this is a breaking change
- [ ] PR description lists known feature repositories that use this component
- [ ] Any affected feature repository submodule update PRs are noted or linked

## Sign-off

- [ ] Reviewed and approved by at least one CODEOWNER before merge
