# WoW Classic Raid Tools

A Windows desktop app for World of Warcraft Classic raid leaders and planners. Keep your guild,
raid groups, raid schedule, BiS lists, gear upgrades and loot log in one place, with a built-in
item database of real tooltips and icons that works offline.

Supports **Classic Era**, **Season of Discovery**, **Forever** (beta), **TBC**, **Wrath**,
**Cataclysm** and **Mists of Pandaria Classic**, in nine languages.

![Dashboard](screenshots/dashboard.png)

## Features

- **Guilds:** import your guild roster from Blizzard (US, EU, Korea or Taiwan realms) and see
  every member's class, race, level and Gear Score. Refresh every character in one go, or add
  members by hand.
- **Character sheets:** each member's equipped gear with full tooltips, gems and enchants, their
  base, melee, spell and defense stats, and resistances. The header sums them up:
  - **Gear Score**, worked out from their item levels with the GearScore / TacoTip formula.
  - **Their main power stat**: bonus healing for healers (gear, gems, enchants and socket bonuses
    added up), spell power for casters, or attack power for melee. Hunters get ranged attack
    power, which Blizzard doesn't report, so it's estimated from their profile.
  - **Item level**.
- **Roster Builder:** drag-and-drop players into raid groups for 10, 20, 25 or 40-player raids,
  or click a player and then a slot. Keep a bench, set roles, add notes per player, and switch to
  a list view with everyone's +1 count. Lock a roster so it can't change by accident, duplicate
  or archive it, and look back at its change history. Link it to the raids it runs.
- **Schedule:** one-off, multi-day or weekly raid nights, optionally tied to a roster. The
  Dashboard shows the next raid and what is coming up.
- **BiS Lists:** import your guild's lists from That's My BiS: its CSV, or its characters export,
  which brings everyone's role too (wishlists and priorities, with loot received marked obtained;
  alts and off-spec optional). No setup needed first: the import can create the guild, add the
  characters it's missing and make a roster for each TMB raid group. Track everyone's progress and
  compare each item with what they have equipped in that slot.
- **Upgrades:** pick any guild member with recorded gear and see, slot by slot, every item that
  would be better for their spec: from raids, dungeons, crafting, vendors, reputation, PvP and
  more, filtered by phase, quality and level. Items are scored with stat weights for each spec in
  each game version (change them, or paste a Pawn string), hit, expertise and a tank's defense
  count only up to their caps, and items on the member's BiS list are marked. It also points out
  missing enchants and empty sockets. Hover an upgrade to see it beside the item it would replace.
  Open it from the page, or from a character sheet.
- **Loot Tracker:** log who got what from which boss, roster by roster, with a +1 system and a
  reset. The boss and item pickers come from the raids the roster runs. **Export for TMB** sends
  the log to That's My BiS's loot import.
- **Attendance:** who was in the raid at each boss kill and everyone's share of the raid nights,
  recorded in game by the [WCRT addon](#in-game-addon-wcrt).
- **Item Database:** 72,000+ items with full tooltips and icons, searchable by name, raid, boss or
  source: dungeons, raids, crafting, vendors, reputation, PvP and more. It includes leveling gear
  at every level and every profession's recipes with the materials they need, plus vendor sell
  prices and filters by quality, slot, type, level, binding and class.
- **Alliance or Horde:** a dark theme in your faction's colors and artwork.
- **Your language:** see [Languages](#languages).
- **In game:** the [WCRT addon](#in-game-addon-wcrt) brings your rosters, BiS lists and loot into the
  game, and records your guild, gear, loot and attendance for the app.

### Import and export

| What | Bring it in from | Take it out as |
|---|---|---|
| Guild roster and characters | Blizzard (by realm and guild name) | — |
| Rosters | A roster file from the app, or a CSV (Name, Class, Role, Server, Notes) | A roster file to share with other officers |
| BiS lists, and the guild and rosters if you don't have them | That's My BiS (its CSV, or its characters export) | — |
| Loot log | — | That's My BiS's loot import (**Export for TMB**) |
| Guild, gear, calendar, loot and attendance | The [WCRT addon](#in-game-addon-wcrt) (`/wcrt export`, or its saved file) | — |
| Rosters, BiS lists, loot and stat weights | — | The WCRT addon (**Guild ▸ Send to Addon**, then `/wcrt import` in game) |
| Everything | A backup file | A backup file of your guilds, rosters, BiS lists and loot log |

Restoring a backup first saves a copy of your current data, in case you need it back.

## In-game addon (WCRT)

**WCRT** is the app's companion addon, for the same game versions. Get it from
[CurseForge](https://www.curseforge.com/wow/addons/wow-classic-raid-tools-wcrt) or
[Wago](https://addons.wago.io/addons/wow-classic-raid-tools-wcrt) (with their apps, it updates itself),
or download the zip from the [addon releases](../../releases?q=addon) and unzip it into your
`Interface\AddOns` folder.

`/wcrt` opens a window laid out like the app, in your faction's colors:

- **Guild, Seen and Schedule:** your roster with notes, the gear of guild members you mouse over or
  inspect, and the in-game calendar with sign-ups.
- **Roster:** invite a roster from the app and sort the raid into its groups.
- **BiS Lists:** who still needs what; item tooltips show **BiS for:** and everyone's **+1s**.
- **Upgrades:** better gear for anyone with recorded gear, scored like the app (stat weights, caps,
  Pawn strings), compared with what they wear.
- **Loot and Attendance:** the loot handed out in raids and who was there at each boss kill,
  recorded as you play.
- **That's My BiS:** paste a TMB export into `/wcrt import` for rosters and BiS lists, and send the
  loot recorded in raids to TMB with `/wcrt export tmb`.
- **Item Database:** every item of your game version, with sources, bosses, sell prices and the
  app's filters.

To bring what it recorded into the app, use **Guilds ▸ Import From Addon** and pick its saved file
(`WTF\Account\<account>\SavedVariables\WCRT.lua`, written when you log out or `/reload`), or paste
what `/wcrt export` shows. The app's **Send to Addon** goes the other way.

Self-hosted servers on the original 1.12 client have their own version: `WCRT-Vanilla-<version>.zip`
on the addon releases.

## Screenshots

| | |
|---|---|
| ![Guild members](screenshots/guild.png) | ![Character sheet](screenshots/character-sheet.png) |
| **Guild:** members, classes and Gear Score | **Character sheet:** equipped gear with tooltips |
| ![Roster Builder](screenshots/roster.png) | ![Loot Tracker](screenshots/loot.png) |
| **Roster Builder:** a 25-player raid in groups | **Loot Tracker:** the loot log with +1s |
| ![BiS progress](screenshots/bis.png) | ![BiS list](screenshots/bis-detail.png) |
| **BiS Lists:** the guild's progress | **BiS list:** each item against what's equipped |
| ![Item Database](screenshots/database.png) | ![Horde theme](screenshots/dashboard-horde.png) |
| **Item Database:** filtered to Serpentshrine Cavern | **Horde theme** |
| ![Upgrades](screenshots/upgrades.png) | ![Settings in German](screenshots/settings-german.png) |
| **Upgrades:** better items for a member's spec, slot by slot | **In German:** Settings, with the language picker |

*The screenshots show an example guild with real TBC Classic items.*

## Languages

The app is available in:

| | |
|---|---|
| English | Русский (Russian) |
| Deutsch (German) | Português (Brasil) |
| Français (French) | 한국어 (Korean) |
| Español (Spanish) | 简体中文 (Simplified Chinese) |
| | 繁體中文 (Traditional Chinese) |

It starts in your Windows language when it's one of these, otherwise in English. Change it any
time in **Settings ▸ Language**. Classes, roles, slots, stats, professions and item qualities use
the game's own names in each language, and dates and numbers follow the language you choose.

Item names and tooltips are still in English in every language. The translations other than
English are drafts: if something reads wrong in your language, please [open an issue](../../issues).

## Install

1. Open the [latest release](../../releases/latest).
2. Download `WoW.Classic.Raid.Tools_<version>_x64-setup.exe` and run it. It installs for your
   Windows user only, so no administrator rights are needed.

Windows may show a SmartScreen warning because the installer isn't code-signed. Choose
**More info ▸ Run anyway**.

## Updates

The app checks for new versions when it starts and offers to install them. You can also check in
**Settings ▸ About & Updates**. Your data is kept when you update.

## Item data

The app's item database is also published on its own, for use in other tools:
[WoW-Classic-Item-Caches](https://github.com/Napalmsteak/WoW-Classic-Item-Caches).

---

This repository only holds the release downloads. The app's source code is private.
World of Warcraft and its item data © Blizzard Entertainment. This is an unofficial, fan-made tool.
