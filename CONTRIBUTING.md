# Contributing to Underground

Thanks for your interest in improving Underground! Contributions of all kinds
are welcome — bug reports, color tweaks, and documentation fixes.

## Repository layout

| Path | What it is |
|------|-----------|
| `editors/vscode/` | The VS Code / Kiro IDE theme extension |
| `editors/vscode/themes/underground-color-theme.json` | The actual color definitions |
| `terminals/windows-terminal/underground.json` | The Windows Terminal color scheme |

## Making changes to the theme

1. Fork and clone the repo.
2. Edit `editors/vscode/themes/underground-color-theme.json`.
3. Test locally by symlinking the extension folder into your editor's
   extensions directory (see the extension README for paths), then reload.
4. If you change any ANSI/terminal colors, mirror them in
   `terminals/windows-terminal/underground.json` so both stay consistent.

## Keeping colors consistent

[`PALETTE.md`](PALETTE.md) is the single source of truth for all colors. Update
it first, then propagate the change to each artifact. The Windows Terminal
scheme is derived from the `terminal.ansi*` values in the VS Code theme — when
you change one, update the other and note it in your PR.

## Commit and PR guidelines

- Use clear, present-tense commit messages (e.g. `fix: soften comment gray`).
- Describe what changed and why in the PR body.
- Include a before/after screenshot for any visible color change.

## Reporting issues

Open an issue with:
- Your editor/terminal and version
- The token or UI element affected
- A screenshot if possible

## License

By contributing, you agree that your contributions are licensed under the
[MIT License](LICENSE).
