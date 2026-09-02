# Underground

A refined minimalist dark theme with a warm green accent. Distraction-free, low-contrast, and consistent across your editor and terminal.

This repository contains two artifacts that share the same palette:

| Artifact | Path | Target |
|----------|------|--------|
| **VS Code / Kiro theme** | [`editors/vscode`](editors/vscode) | VS Code, Kiro IDE |
| **Windows Terminal scheme** | [`terminals/windows-terminal`](terminals/windows-terminal) | Windows Terminal (PowerShell, CMD, WSL) |

## Palette

| Role | Hex |
|------|-----|
| Background | `#222222` |
| Foreground | `#ffffffde` |
| Keywords / Tags / Parameters | `#9bd4b2` |
| Strings / Functions / Numbers | `#90aed3` |
| Types / Attributes | `#ceb0d3` |
| Comments | `#6a6a6a` |
| Errors | `#e29090` |
| Warnings | `#f7df9b` |
| Info / Links | `#81a2be` |
| Selection / find match | `#353535` |

> Note: the editor background is `#222222`; the deep `#1a1a1a` is reserved for
> the terminal's `ansiBlack`. The Windows Terminal scheme also uses `#222222`
> as its background to match the editor chrome.

The full palette — base colors, syntax roles, and terminal ANSI values — is
documented in [PALETTE.md](PALETTE.md), the single source of truth for all
artifacts.

## Installation

- **VS Code / Kiro IDE** — see [`editors/vscode/README.md`](editors/vscode/README.md)
- **Windows Terminal** — see [`terminals/windows-terminal/README.md`](terminals/windows-terminal/README.md)

## Contributing

Contributions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Changelog

Project-wide history is in [CHANGELOG.md](CHANGELOG.md). The VS Code extension
also keeps a marketplace-facing changelog at
[`editors/vscode/CHANGELOG.md`](editors/vscode/CHANGELOG.md).

## License

[MIT](LICENSE) © Indiorlei
