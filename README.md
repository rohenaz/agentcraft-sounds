# agentcraft-sounds

A curated sound library for [AgentCraft](https://github.com/rohenaz/agentcraft) — assign sounds to Claude Code lifecycle events.

## Setup

AgentCraft downloads this library automatically on first run (`/agentcraft`). To install manually or update:

```bash
# First install
git clone https://github.com/rohenaz/agentcraft-sounds ~/.agentcraft/sounds

# Update later
git -C ~/.agentcraft/sounds pull
```

Then install AgentCraft:

```bash
claude plugin install agentcraft@rohenaz
```

Open the dashboard with `/agentcraft` and start assigning sounds.

## Library Contents

```
agentcraft-sounds/
  sc2/                  StarCraft II sounds
    terran/
    protoss/
    zerg/
  wc3/                  Warcraft III sounds
  ff7/                  Final Fantasy VII sounds
  ff9/                  Final Fantasy IX sounds
  apps/                 Nostalgic app sounds
    aim/                AIM door open/close
    icq/                ICQ "uh oh"
    winamp/
  classic-os/           Classic operating system sounds
    mac/                Mac startup chime, classic sounds
    windows/            Win95, XP, jungle/utopia startups
  phones/               Nostalgic mobile device sounds
    nokia/alerts/       Nokia alert tones
    motorola/           Motorola button sounds
    pager/              Pager beeps and blips
  ui/                   UI theme sounds (used by AgentCraft themes)
    sc2/                StarCraft II UI theme
    wc3/                Warcraft III UI theme
    ff7/                Final Fantasy VII UI theme
    ff9/                Final Fantasy IX UI theme
    sc-bigbox/          SC BigBox alternate set
```

## UI Themes

The `ui/` directory contains themed sets for AgentCraft's interface sounds. Each theme needs these slots (all under `ui/{theme}/`):

| File | Slot |
|------|------|
| `hover.mp3` | Mouse-over sound |
| `click.mp3` | Button click |
| `error.mp3` | Error / failure |

Optional (no default, must be assigned in configurator):
- `pageChange.mp3` — tab navigation
- `toggle.mp3` — expand/collapse
- `confirm.mp3` — assignment confirmed, saved

## Adding Your Own Sounds

Drop audio files anywhere under `~/.agentcraft/sounds/`. AgentCraft scans the entire directory — any `.mp3`, `.wav`, `.ogg`, or `.m4a` file appears in the browser automatically.
