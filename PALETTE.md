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
| Selection / find match | `#2c3a30` (selection), `#353535` (find match) | `editor.selectionBackground`, `editor.findMatchBackground` |
| Deep black | `#1a1a1a` | terminal `ansiBlack` |
| Foreground | `#ffffffde` | primary text (white, ~87% alpha) |
| Foreground (muted) | `#ffffff99` | secondary text (~60% alpha) |
| Foreground (subtle) | `#ffffff61` | tertiary text (~38% alpha) |
| Comment / bright black | `#6a6a6a` | comments, `ansiBrightBlack` |
| Line numbers | `#5a5a5a` (inactive), `#ffffffde` (active) | `editorLineNumber.foreground`, `editorLineNumber.activeForeground` |
| Focus border | `#3a3a3a` | `focusBorder` (keyboard nav) |
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

### Diff & merge

The diff editor tints added/removed content with the git colors above, at low
alpha so the background stays calm. Line-level highlights are subtler than
word-level ones:

| Role | Hex | Where |
|------|-----|-------|
| Inserted text (word) | `#b5bd6861` | `diffEditor.insertedTextBackground` |
| Inserted line | `#b5bd6815` | `diffEditor.insertedLineBackground` |
| Removed text (word) | `#e2909061` | `diffEditor.removedTextBackground` |
| Removed line | `#e2909015` | `diffEditor.removedLineBackground` |
| Diff border / diagonal fill | `#2e2e2e` | `diffEditor.border`, `diffEditor.diagonalFill` |

Merge conflicts reuse the palette semantically — **current** (local) uses the
green accent, **incoming** uses info blue, **common** (base) stays neutral
gray, and unresolved conflict borders use the warning yellow:

| Role | Hex | Where |
|------|-----|-------|
| Current header / content | `#9bd4b233` / `#9bd4b21a` | `merge.current*Background` |
| Incoming header / content | `#81a2be33` / `#81a2be1a` | `merge.incoming*Background` |
| Common header / content | `#3a3a3a` / `#2c2c2c` | `merge.common*Background` |
| Merge border | `#2e2e2e` | `merge.border` |
| Conflict border (unhandled) | `#f7df9b` / `#f7df9b66` | `mergeEditor.conflict.unhandled*.border` |
| Conflict border (handled) | `#6a6a6a` / `#3a3a3a` | `mergeEditor.conflict.handled*.border` |

### Input validation

Validation messages use a dark tonal background with the accent color on the
border only (keeps the message text readable):

| Role | Background | Border |
|------|-----------|--------|
| Error | `#2e2222` | `#e29090` |
| Warning | `#2e2b22` | `#f7df9b` |
| Info | `#22282e` | `#81a2be` |

## Terminal ANSI colors

Source for the Windows Terminal scheme
(`terminals/windows-terminal/underground.json`), mirroring the `terminal.ansi*`
keys in the VS Code theme.

| ANSI | Normal | Bright |
|------|--------|--------|
| Black | `#1a1a1a` | `#6a6a6a` |
| Red | `#e29090` | `#e29090` |
| Green | `#9bd4b2` | `#9bd4b2` |
| Yellow | `#f7df9b` | `#f7df9b` |
| Blue | `#90aed3` | `#90aed3` |
| Magenta / Purple | `#ceb0d3` | `#ceb0d3` |
| Cyan | `#8abeb7` | `#8abeb7` |
| White | `#d4d4d4` | `#d4d4d4` |

Bright variants share the hue of their normal counterpart, except
`brightBlack` (`#6a6a6a`). The standalone Windows Terminal scheme also sets
`brightWhite` to `#ffffff` and uses `#222222` as its background to match the
editor chrome.

> **Note:** `#8abeb7` (cyan) appears only in the terminal ANSI set, not in the
> editor's syntax tokens. The ANSI yellow uses `#f7df9b`, the same warm yellow as
> the editor's warning color, keeping a single yellow across the theme.

## Where each color lives

| Artifact | File |
|----------|------|
| VS Code / Kiro theme (canonical) | `editors/vscode/themes/underground-color-theme.json` |
| Windows Terminal scheme | `terminals/windows-terminal/underground.json` |
