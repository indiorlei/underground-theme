# Indio Minimal

A refined minimalist dark theme for VS Code and Kiro IDE, inspired by [Minimal](https://marketplace.visualstudio.com/items?itemName=nichabosh.minimalist-dark) by nichabosh.

## Preview

### Palette

| Role | Color | Hex |
|------|-------|-----|
| Background | ⬛ | `#1a1a1a` |
| Foreground | ⬜ | `#d4d4d4` |
| Keywords/Tags | 🟢 | `#9bd4b2` |
| Strings/Functions | 🔵 | `#90aed3` |
| Types/Attributes | 🟣 | `#ceb0d3` |
| Constants/Numbers | 🟠 | `#d4a07a` |
| Operators | 🩵 | `#8abeb7` |
| Errors | 🔴 | `#e29090` |
| Warnings | 🟡 | `#f0c674` |
| Accent (selection) | 🌿 | `#3a7d5c` |

## Changes from Minimal (nichabosh)

- Darker background (`#1a1a1a` vs `#222222`) for deeper contrast
- Green accent (`#3a7d5c`) for selections, find matches, and active borders
- Separate color for constants/numbers (`#d4a07a`) — warm orange tone
- Operators get their own color (`#8abeb7` cyan)
- Comments in italic with subtler gray
- `this`/`super` highlighted in red italic
- Semantic highlighting enabled for better TypeScript/JS support
- More refined borders with subtle separations
- Cursor and terminal cursor in green (`#9bd4b2`)

## Installation

### VS Code / Kiro IDE

1. Copy this folder to your extensions directory:
   - **macOS**: `~/.vscode/extensions/` or `~/.kiro/extensions/`
   - **Linux**: `~/.vscode/extensions/` or `~/.kiro/extensions/`
   - **Windows**: `%USERPROFILE%\.vscode\extensions\` or `%USERPROFILE%\.kiro\extensions\`

2. Restart VS Code / Kiro IDE

3. Open Command Palette (`Cmd+Shift+P`) → "Preferences: Color Theme" → Select **Indio Minimal**

### Alternative: Symlink (for development)

```bash
# VS Code
ln -s ~/projects/personal/indio-minimal-theme ~/.vscode/extensions/indio-minimal-theme

# Kiro IDE
ln -s ~/projects/personal/indio-minimal-theme ~/.kiro/extensions/indio-minimal-theme
```

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

## Credits

Based on [Minimal](https://marketplace.visualstudio.com/items?itemName=nichabosh.minimalist-dark) by nichabosh.

## License

MIT
