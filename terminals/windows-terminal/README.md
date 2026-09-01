# Underground — Windows Terminal

A color scheme for **Windows Terminal** (PowerShell, CMD, WSL) matching the
[Underground](../../editors/vscode) VS Code theme.

## Palette

| Role              | Hex       |
|-------------------|-----------|
| Background        | `#222222` |
| Foreground        | `#D4D4D4` |
| Cursor            | `#9BD4B2` |
| Selection         | `#353535` |
| Black             | `#1A1A1A` |
| Red               | `#E29090` |
| Green             | `#9BD4B2` |
| Yellow            | `#D4A07A` |
| Blue              | `#90AED3` |
| Purple / Magenta  | `#CEB0D3` |
| Cyan              | `#8ABEB7` |
| White             | `#D4D4D4` |

Bright variants share the same hues; `brightBlack` is `#6A6A6A` and
`brightWhite` is `#FFFFFF`.

## Installation

### Via the settings UI

1. Open Windows Terminal → `Ctrl+,` (or dropdown → **Settings**).
2. In the left panel, scroll to **Color schemes** → **Add new**.
3. Enter the values from `underground.json` (or use the JSON method below).

### Via settings.json (recommended)

1. Open Windows Terminal → dropdown → **Settings** → click **Open JSON file**
   (bottom-left gear), or edit directly:
   ```
   %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json
   ```
2. Copy the object from `underground.json` into the top-level `"schemes"` array:
   ```json
   {
     "schemes": [
       {
         "name": "Underground",
         "background": "#222222",
         "foreground": "#D4D4D4",
         "cursorColor": "#9BD4B2",
         "selectionBackground": "#353535",
         "black": "#1A1A1A",
         "red": "#E29090",
         "green": "#9BD4B2",
         "yellow": "#D4A07A",
         "blue": "#90AED3",
         "purple": "#CEB0D3",
         "cyan": "#8ABEB7",
         "white": "#D4D4D4",
         "brightBlack": "#6A6A6A",
         "brightRed": "#E29090",
         "brightGreen": "#9BD4B2",
         "brightYellow": "#D4A07A",
         "brightBlue": "#90AED3",
         "brightPurple": "#CEB0D3",
         "brightCyan": "#8ABEB7",
         "brightWhite": "#FFFFFF"
       }
     ]
   }
   ```
3. Apply it to a profile by setting `"colorScheme": "Underground"` inside that
   profile, or under `"profiles": { "defaults": { ... } }` to apply everywhere.
4. Save. Windows Terminal reloads automatically.

## Recommended profile settings

```json
{
  "profiles": {
    "defaults": {
      "colorScheme": "Underground",
      "font": {
        "face": "JetBrains Mono",
        "size": 11
      },
      "cursorShape": "bar",
      "padding": "12"
    }
  }
}
```

## Notes

- The scheme is derived from the `terminal.ansi*` values of the VS Code theme,
  so colors stay consistent between the editor's integrated terminal and
  Windows Terminal.
- Works with PowerShell, CMD and WSL profiles.
- For a richer PowerShell prompt, pair it with
  [Oh My Posh](https://ohmyposh.dev/) or `PSReadLine` — this scheme only sets
  the terminal colors, not the shell prompt.
