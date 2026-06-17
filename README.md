# The Enceladeum Dalamud Plugin Repository

A single custom-repository feed for all of **The Enceladeum**'s FFXIV / Dalamud
plugins. Add the one URL below and every plugin here shows up in the in-game
installer and any plugin added later appears automatically.

## Installing

1. In game, open `/xlsettings` → **Experimental** → **Custom Plugin Repositories**.
2. Paste this URL into a new row, click the **+**, then **Save**:

   ```
   https://raw.githubusercontent.com/Enceladeum/DalamudPlugins/main/repo.json
   ```
3. Open the plugin installer (`/xlplugins`) and install any plugin listed below.

> **Add only this one URL.** This feed already lists every plugin. If you
> previously added a per-plugin URL (e.g. the HOutfits or HClawsweep repo
> directly), you can keep it — those still work and list the same builds — but
> you don't need both. One subscription is enough.

## Plugins

| Plugin | Command(s) | What it does |
| --- | --- | --- |
| **HOutfits** | `/houtfits` | Apply a complete named outfit set — or any single piece — to your character through [Glamourer](https://github.com/Ottermandias/Glamourer) in one click. Requires Glamourer. |
| **Cosmic Claw** | `/clawsweep`, `/clawsweeploop` | Play the Cosmic Predator's Magitek *Claw Sweep* animation on demand — once or on a loop — while mounted on it. Purely cosmetic and local-only. |

Each plugin keeps its own repository, releases, and issue tracker; this feed is
just the shared index that points at them:

- HOutfits - https://github.com/Enceladeum/HOutfits
- Cosmic Claw (HClawsweep) - https://github.com/Enceladeum/HClawsweep

## How this feed works

A Dalamud custom repository is a single JSON file ([`repo.json`](repo.json)) that
holds an **array** of plugin manifests. Dalamud reads the array and offers every
entry to anyone subscribed to the URL. Each entry's `DownloadLinkInstall` points
at that plugin's own GitHub releases, so the actual plugin zips are never hosted
here, only the index. Publishing a new plugin (or a new version) is a matter of
adding/updating its entry in this file.

## License

MIT — see [LICENSE](LICENSE). Individual plugins are licensed in their own
repositories.
