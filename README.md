# Enhanced Shots

[![Project Status: Inactive – The project has reached a stable, usable state but is no longer being actively developed.](https://www.repostatus.org/badges/latest/inactive.svg)](https://www.repostatus.org/#inactive)
[![Unity 2021.3 LTS](https://img.shields.io/badge/Unity-2021.3%20LTS-000000.svg?logo=unity&logoColor=white)](https://unity.com/releases/editor/qa/lts-releases)
[![C#](https://img.shields.io/badge/C%23-239120.svg?logo=csharp&logoColor=white)](https://learn.microsoft.com/dotnet/csharp/)
[![Play in the browser](https://img.shields.io/badge/play-WebGL-654FF0.svg?logo=webgl&logoColor=white)](https://andersongacfilho.github.io/play/enhanced-shots)
[![itch.io](https://img.shields.io/badge/itch.io-Vertex%20Shift-FA5C5C.svg?logo=itchdotio&logoColor=white)](https://vertex-shift.itch.io/enhanced-shots)
[![Course: UFG](https://img.shields.io/badge/course-UFG%20Jogos%20Digitais%202023.1-0A9EDC.svg)](https://www.ufg.br/)
[![Team: WMDG](https://img.shields.io/badge/team-WMDG-6A5ACD.svg)](https://github.com/rafaeljcoutinho/WMDG)
[![Fork](https://img.shields.io/badge/fork-of%20rafaeljcoutinho%2FWMDG-FF7F50.svg?logo=github&logoColor=white)](https://github.com/rafaeljcoutinho/WMDG)

First-person shooting gallery built in Unity, where the targets are the
mechanic: each one does something different when it breaks, so the choice of
what to shoot matters more than the aim.

> **This is a fork.** The project belongs to **WMDG**, a four-person team from
> the Digital Games course at UFG, 2023.1. The canonical repository is
> [rafaeljcoutinho/WMDG](https://github.com/rafaeljcoutinho/WMDG); this fork
> tracks it without divergence and exists so the work stays reachable from my
> portfolio. The section below states only what I wrote.

## The targets

Shooting is easy. Reading the board is the game: ammunition is finite, the
clock is running, and every target is a different trade.

| Target            | Effect on break                       |
|-------------------|----------------------------------------|
| `TargetNormal`    | Plain score.                           |
| `Target2xPoints`  | Doubles the points awarded.            |
| `Target8Ammo`     | Refills ammunition.                    |
| `TargetClock`     | Buys time.                             |
| `TargetBombIt`    | Detonates, taking neighbours with it.  |
| `TargetTurttle`   | Slows the pace down.                   |
| `TargetLucky`     | Gambles: the payout is not fixed.      |

## Modes and flow

`Menu` opens onto `ModeSelector`, which leads either to the standard
`GameScene` or to `LuckyModeScene`. A run ends in `FinishRound`, which writes
the result before `HighscoreScene` ranks it. `WeaponSelector` and
`WeaponsCrate` handle loadout, `ConfigScene` the settings.

Scores persist between sessions as JSON, through `SaveMethod` and
`PlayerData`.

## What I contributed

Of 122 commits, 42 are mine, which makes me the largest contributor by count.
The work I am accountable for:

- **Lucky Mode** — the alternate mode built around the gamble target, from
  the scene to the scoring rules.
- **Run completion screen** — the end-of-run flow that closes a session and
  hands the result to the highscore table.
- **Highscore integration** — wiring persisted scores into the ranking screen
  on top of the JSON save Rafael had introduced.
- **Background music and card icons** — the audio pass and the iconography on
  the selection cards.

The special target set itself is **Rafael Coutinho's**, as is the original
JSON save. Crediting that properly matters more than a longer list.

## Team

| Contributor | Commits |
|-------------|---------|
| Anderson Gonçalves | 42 |
| Rafael Coutinho | 38 |
| Pedro Costa e Faustino | 26 |
| Bryan Bento | 16 |

## Playing it

A WebGL build runs in the browser at
[andersongacfilho.github.io/play/enhanced-shots](https://andersongacfilho.github.io/play/enhanced-shots),
or on [itch.io](https://vertex-shift.itch.io/enhanced-shots).

To open the sources, Unity **2021.3.29f1** is the version the project was
authored against.

## Project material

The team's planning artefacts, kept as they were:

- [Drive](https://drive.google.com/drive/folders/1wSq8_EmP8yq9YMTKMyuBPXC_MkdH7ntw?usp=sharing)
- [Trello](https://trello.com/b/wBEHf3HP/wmdg)
- [Notion](https://shorthaired-gasosaurus-ac7.notion.site/UFG-Jogos-Digitais-b4c6e98e5aef4f4c82e2bad8dcfcc690)
- [Pitch](https://drive.google.com/file/d/1DijsguBy01sGVY8vKvxueyZyp_Ibt6MS/view?usp=share_link)
- [Figma prototypes](https://www.figma.com/file/fi8sL0KyBQVKQM0M2LznAw/Untitled?t=6iEKbVOz83cI5SEX-1)
