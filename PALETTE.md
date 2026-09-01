# Palette

Single source of truth for the **Underground** color palette.

The VS Code / Kiro theme
(`editors/vscode/themes/underground-color-theme.json`) is the canonical source.
Every other artifact (Windows Terminal scheme and any future targets) derives
its colors from the values documented here.

When you change a color, update the VS Code theme first, then reflect it here
and propagate it to the other artifacts. Note the change in the relevant
`CHANGELOG`.

## Base colors (editor UI)

| Role | Hex | Where |
|------|-----|-------|
| Background | `#222222` | `editor.background`, panels, sidebar, tabs |
| Surface (raised) | `#272727` | inputs, status bar, active tab, widgets |
| Surface (hover/drop) | `#2e2e2e` | hover, selected suggest, drop target |
| Selection / find match | `#353535` | `editor.selectionBackground`, `editor.findMatchBackground` |
| Deep black | `#1a1a1a` | terminal `ansiBlack` |
| Foreground | `#ffffffde` | primary text (white, ~87% alpha) |
| Foreground (muted) | `#ffffff99` | secondary text (~60% alpha) |
| Foreground (subtle) | `#ffffff61` | tertiary text (~38% alpha) |
| Comment / bright black | `#6a6a6a` | comments, `ansiBrightBlack` |
| Line numbers | `#333333` | `editorLineNumber.foreground` |
| Cursor | `#ffffffde` | `editorCursor.foreground` |
| Green accent | `#9bd4b2` | active borders (`panelTitle.activeBorder`), git modified |

## Syntax roles (tokenColors)

Colors actually applied to code in the editor:

| Role | Hex | Swatch | Scopes |
|------|-----|--------|--------|
| Keywords / Storage / Parameters / Tags | `#9bd4b2` | 🟢 | `keyword`, `storage.*`, `variable.parameter`, `entity.name.tag` |
| Strings / Functions / Numbers / Constants / `this` | `#90aed3` | 🔵 | `string`, `support.function`, `constant.numeric`, `variable.language.this` |
| Types / Interfaces / Enums / Attributes | `#ceb0d3` | 🟣 | `entity.name.type`, `meta.function-call`, `entity.other.attribute-name` |
| Comments | `#6a6a6a` | ⚫ | `comment`, `punctuation.definition.comment` |

### Semantic token colors

| Token | Hex |
|-------|-----|
| type / interface / enum | `#ceb0d3` |
| function / method | `#90aed3` |
| variable.readonly / enumMember | `#90aed3` |
| parameter | `#9bd4b2` |
| namespace / property / variable | `#ffffffde` |

## Diagnostic & status colors

| Role | Hex | Swatch |
|------|-----|--------|
| Error | `#e29090` | 🔴 |
| Warning | `#f7df9b` | 🟡 |
| Info / Links | `#81a2be` | 🔵 |
| Git added | `#b5bd68` | 🟢 |
| Git modified | `#9bd4b2` | 🟢 |
| Git deleted | `#e29090` | 🔴 |

## Terminal ANSI colors

Source for the Windows Terminal scheme
(`terminals/windows-terminal/underground.json`), mirroring the `terminal.ansi*`
keys in the VS Code theme.

| ANSI | Normal | Bright |
|------|--------|--------|
| Black | `#1a1a1a` | `#6a6a6a` |
| Red | `#e29090` | `#e29090` |
| Green | `#9bd4b2` | `#9bd4b2` |
| Yellow | `#d4a07a` | `#d4a07a` |
| Blue | `#90aed3` | `#90aed3` |
| Magenta / Purple | `#ceb0d3` | `#ceb0d3` |
| Cyan | `#8abeb7` | `#8abeb7` |
| White | `#d4d4d4` | `#d4d4d4` |

Bright variants share the hue of their normal counterpart, except
`brightBlack` (`#6a6a6a`). The standalone Windows Terminal scheme also sets
`brightWhite` to `#ffffff` and uses `#222222` as its background to match the
editor chrome.

> **Note:** `#8abeb7` (cyan) and `#d4a07a` (warm yellow/orange) currently appear
> only in the terminal ANSI set, not in the editor's syntax tokens.

## Where each color lives

| Artifact | File |
|----------|------|
| VS Code / Kiro theme (canonical) | `editors/vscode/themes/underground-color-theme.json` |
| Windows Terminal scheme | `terminals/windows-terminal/underground.json` |
