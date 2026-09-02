# Underground

A refined minimalist dark theme for VS Code and Kiro IDE. Low-contrast, distraction-free, with a warm green accent.

## Preview

![Underground theme preview](images/preview.png)

### Palette

| Role | Color | Hex |
|------|-------|-----|
| Background | ⬛ | `#222222` |
| Foreground | ⬜ | `#ffffffde` |
| Keywords/Tags/Parameters | 🟢 | `#9bd4b2` |
| Strings/Functions/Numbers | 🔵 | `#90aed3` |
| Types/Attributes | 🟣 | `#ceb0d3` |
| Comments | ⚫ | `#6a6a6a` |
| Errors | 🔴 | `#e29090` |
| Warnings | 🟡 | `#f7df9b` |
| Info/Links | 🔵 | `#81a2be` |
| Selection/find match | 🌫️ | `#353535` |

## Highlights

- Warm, low-contrast dark background (`#222222`) that reduces eye strain
- Green (`#9bd4b2`) for keywords, tags, and parameters
- Blue (`#90aed3`) for strings, functions, numbers, and `this`
- Purple (`#ceb0d3`) for types, classes, and attributes
- Comments in italic with a subtle gray (`#6a6a6a`)
- Green active borders (`#9bd4b2`) on focused panels
- Semantic highlighting enabled for better TypeScript/JS support
- Matching Windows Terminal color scheme

## Installation

This theme is distributed through GitHub (it is not on the Marketplace). Pick
whichever option suits you — they all end with the same result.

After installing by any method, select the theme:
**Command Palette** (`Ctrl+Shift+P` / `Cmd+Shift+P`) →
`Preferences: Color Theme` → **Underground**.

### Option 1 — Install from a `.vsix` file (recommended)

The easiest way. A packaged `.vsix` is attached to each
[GitHub Release](https://github.com/indiorlei/underground-theme/releases).

1. Download the latest `underground-theme-<version>.vsix` from the Releases page.
2. In VS Code / Kiro IDE, open the **Extensions** view (`Ctrl+Shift+X`).
3. Click the `⋯` menu (top-right of the panel) → **Install from VSIX…**
4. Select the downloaded file.

Or from the command line:

```bash
code --install-extension underground-theme-<version>.vsix
```

> Note: `.vsix` installs do not auto-update. To update, download the newer
> `.vsix` and install it again.

### Option 2 — Copy the folder into your extensions directory

Clone (or download) this repository, then copy the `editors/vscode` folder into
your editor's extensions directory:

- **Windows**: `%USERPROFILE%\.vscode\extensions\` or `%USERPROFILE%\.kiro\extensions\`
- **macOS / Linux**: `~/.vscode/extensions/` or `~/.kiro/extensions/`

```bash
git clone https://github.com/indiorlei/underground-theme.git
# Windows (PowerShell)
Copy-Item -Recurse underground-theme/editors/vscode "$env:USERPROFILE/.vscode/extensions/underground-theme"
# macOS / Linux
cp -r underground-theme/editors/vscode ~/.vscode/extensions/underground-theme
```

Then restart VS Code / Kiro IDE.

### Option 3 — Symlink (best for development)

If you plan to tweak the theme, symlink the folder so your edits are picked up
without copying:

```bash
# VS Code
ln -s "$(pwd)/underground-theme/editors/vscode" ~/.vscode/extensions/underground-theme

# Kiro IDE
ln -s "$(pwd)/underground-theme/editors/vscode" ~/.kiro/extensions/underground-theme
```

On Windows (PowerShell, as administrator):

```powershell
New-Item -ItemType SymbolicLink -Path "$env:USERPROFILE/.vscode/extensions/underground-theme" -Target "$(Get-Location)/underground-theme/editors/vscode"
```

Then restart the editor.

## Recommended Settings

```json
{
  "editor.fontFamily": "JetBrains Mono, Fira Code, monospace",
  "editor.fontSize": 13,
  "editor.lineHeight": 1.6,
  "editor.cursorBlinking": "phase",
  "editor.bracketPairColorization.enabled": false,
  "editor.minimap.enabled": false,
  "editor.renderWhitespace": "none",
  "editor.overviewRulerBorder": false,
  "workbench.tree.indent": 16
}
```

## License

MIT — see [LICENSE](../../LICENSE).
