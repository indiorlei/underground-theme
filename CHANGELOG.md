# Changelog

All notable changes to the **Underground** project are documented here. This is
the project-wide changelog, covering every artifact (the VS Code / Kiro theme,
the Windows Terminal scheme, and shared assets such as the palette and docs).

The VS Code extension also keeps its own, marketplace-facing changelog at
[`editors/vscode/CHANGELOG.md`](editors/vscode/CHANGELOG.md); entries there focus
strictly on the published extension.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.2.0] - 2026-09-02

### Added
- Diff editor border and diagonal fill (`diffEditor.border`,
  `diffEditor.diagonalFill`) so the diff chrome matches the low-contrast theme.
- Merge conflict colors (`merge.*`, `mergeEditor.*`) derived from the palette:
  current uses the green accent, incoming the info blue, common a neutral gray,
  and unresolved conflict borders the warning yellow.
- `PALETTE.md` "Diff & merge" section documenting all diff and merge colors.

### Fixed
- Diff inserted-line background used the "git modified" green (`#9bd4b2`) instead
  of the "git added" green (`#b5bd68`); now consistent with the palette.

## [1.1.1] - 2026-09-02

### Fixed
- Line numbers were nearly invisible (`#333333`); raised to `#5a5a5a` with an
  active line number color (`#ffffffde`).
- Input validation popups used saturated backgrounds with unreadable text; now
  dark tonal backgrounds with the accent on the border only.
- `focusBorder` matched the background, hiding keyboard focus; set to `#3a3a3a`.
- `listFilterWidget` used a solid blue background; now neutral with a colored
  outline.

### Changed
- Editor selection uses a subtle green tint (`#2c3a30`).
- Unified the terminal ANSI yellow with the UI warning color (`#f7df9b`) across
  the theme and the Windows Terminal scheme.
- Normalized all hex color values to lowercase.

## [1.1.0] - 2026-09-01

### Added
- Semantic highlighting support for better TypeScript/JS token coloring.
- Windows Terminal color scheme matching the editor palette.
- `PALETTE.md` as the single source of truth for all artifacts.

### Changed
- Repository restructured into a monorepo (`editors/`, `terminals/`) and
  prepared for public release under the name **Underground**.
- Green accent (`#9bd4b2`) applied to active panel borders.
- Comments rendered in italic with a subtle gray (`#6a6a6a`).

## [1.0.0] - 2026-08-30

### Added
- Initial release of the Underground dark theme for VS Code and Kiro IDE.
