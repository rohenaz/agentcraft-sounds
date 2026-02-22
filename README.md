# agentcraft-sounds

The official sound library for [AgentCraft](https://github.com/rohenaz/agentcraft) — assign sounds to Claude Code lifecycle events.

This is a **sound pack**. AgentCraft installs it automatically on first run.

## Setup

Installed automatically when you run `/agentcraft` for the first time. To install manually or update:

```bash
# Install
agentcraft pack install rohenaz/agentcraft-sounds

# Update
agentcraft pack update rohenaz/agentcraft-sounds
```

Or with plain git (same result):

```bash
git clone https://github.com/rohenaz/agentcraft-sounds ~/.agentcraft/packs/rohenaz/agentcraft-sounds
git -C ~/.agentcraft/packs/rohenaz/agentcraft-sounds pull
```

## Contents

```
agentcraft-sounds/
  sc2/                  StarCraft II sounds (terran, protoss, zerg)
  wc3/                  Warcraft III sounds
  ff7/                  Final Fantasy VII sounds
  ff9/                  Final Fantasy IX sounds
  apps/                 Nostalgic app sounds (AIM, ICQ, Winamp)
  classic-os/           Mac and Windows startup/UI sounds
  phones/               Nokia alerts, Motorola buttons, pager beeps
  ui/                   UI theme sounds
    sc2/                StarCraft II UI theme
    wc3/                Warcraft III UI theme
    ff7/                Final Fantasy VII UI theme
    ff9/                Final Fantasy IX UI theme
    sc-bigbox/          SC BigBox alternate set
  defaults/
    assignments.json    Starter configuration for new installs
```

## UI Themes

The `ui/` directory powers AgentCraft's ambient interface sounds. Each theme directory needs:

| File | Slot |
|------|------|
| `hover.mp3` | Mouse-over |
| `click.mp3` | Button click |
| `error.mp3` | Error / failure |

Optional (silent unless explicitly assigned in the dashboard):
- `pageChange.mp3` — tab navigation
- `toggle.mp3` — expand/collapse rows
- `confirm.mp3` — assignment saved

## Creating Your Own Pack

A sound pack is just a git repo. No manifest required.

1. Create a GitHub repo with your sound files (`.mp3`, `.wav`, `.ogg`, `.m4a`)
2. Organize however you like — AgentCraft scans recursively
3. Share it as `your-username/your-repo-name`

Users install it with:
```bash
agentcraft pack install your-username/your-repo-name
```

For a UI theme pack, add a `ui/<theme-name>/` directory with `hover.mp3`, `click.mp3`, and `error.mp3`. The theme name appears automatically in the AgentCraft theme selector.
