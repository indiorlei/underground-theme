# Changelog

All notable changes to the **Underground** theme are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.2.0] - 2026-09-02

### Added
- Merge conflict colors (`merge.*`, `mergeEditor.*`), previously unset and
  falling back to VS Code's saturated defaults. Now derived from the palette:
  current uses the green accent, incoming the info blue, common a neutral gray,
  and unresolved conflict borders the warning yellow.
- Diff editor border and diagonal fill (`diffEditor.border`,
  `diffEditor.diagonalFill`), set to `#2e2e2e` so the diff chrome matches the
  low-contrast theme instead of the editor default.

### Fixed
- Diff inserted-line background used the "git modified" green (`#9bd4b2`) instead
  of the "git added" green (`#b5bd68`); aligned with the palette so inserted text
  and inserted lines share the same hue.

### Changed
- Documented all diff and merge colors in `PALETTE.md`.

## [1.1.1] - 2026-09-02

### Fixed
- Line numbers were nearly invisible (`#333333`); raised to `#5a5a5a` and added
  an active line number color (`#ffffffde`).
- Input validation popups used solid saturated backgrounds with unreadable text
  (notably the warning). Now use dark tonal backgrounds with the accent on the
  border only.
- `focusBorder` matched the background, leaving keyboard focus invisible; set to
  `#3a3a3a`.
- `listFilterWidget` used a solid blue background; now neutral (`#272727`) with a
  colored outline.

### Changed
- Editor selection uses a subtle green tint (`#2c3a30`) for better visibility.
- Unified the terminal ANSI yellow (`#d4a07a` → `#f7df9b`) with the UI warning
  color, giving a single, higher-contrast yellow that matches the theme's pastel
  palette. Propagated to the Windows Terminal scheme.
- Normalized all hex color values to lowercase for consistency.

## [1.1.0] - 2026-09-01

### Added
- Semantic highlighting support for better TypeScript/JS token coloring.
- Matching Windows Terminal color scheme.

### Changed
- Green (`#9bd4b2`) applied to active panel borders.
- Comments rendered in italic with a subtle gray (`#6a6a6a`).
- Refined borders with subtle separations.

## [1.0.0] - 2026-08-30

### Added
- Initial release of the Underground dark theme for VS Code and Kiro IDE.
