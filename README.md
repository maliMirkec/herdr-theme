# Cita themes for Herdr

Cita light and dark themes for the Herdr desktop app.

## Files

- `cita-light.json`
- `cita-dark.json`

## Install

Copy the files to the Herdr themes folder:

```sh
cp cita-*.json ~/.config/herdr-app/themes/
```

## Apply

```sh
herdr-app do app.theme '{"name":"cita-light"}'
herdr-app do app.theme '{"name":"cita-dark"}'
```

## Format

Each theme is a JSON file with these keys:

- `background`
- `foreground`
- `selection`
- `cursor`
- `ansi`, a list of 16 colors
- `colors`, a map of UI color overrides

You can find all `colors` keys in `~/.config/herdr-app/herdr.d.ts`, under `theme()`. The full guide is in `~/.config/herdr-app/AGENTS.md`.

## Where the colors come from

The base colors come from the etty themes in `marta-themes`:

- `CitaLight.ettyTheme` → `cita-light.json`
- `CitaDark.ettyTheme` → `cita-dark.json`

Keys map like this:

| etty | Herdr |
| --- | --- |
| `background` | `background` |
| `foreground` | `foreground` |
| `selection` | `selection` |
| `caret` | `cursor` |
| `ansiColors` | `ansi` |

## Mint overrides

The `colors` map adds extra mint to the UI:

| Key | Light | Dark |
| --- | --- | --- |
| `accent` | `#08805a` | `#63f2c5` |
| `accent_foreground` | `#ffffff` | `#011d3b` |
| `chrome` | `#e0fcf3` | none |
| `hover` | `#c4f5e9` | `#1a535e` |
| `selected` | `#9bf7da` | `#0f6652` |
| `done` | `#08805a` | `#63f2c5` |

## Note

The Herdr desktop app is not the herdr.dev TUI. The TUI docs for `~/.config/herdr/config.toml` and `[theme.custom]` don't apply here.
