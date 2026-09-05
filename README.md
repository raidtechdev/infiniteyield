# INFY 2.0

A heavily modified fork of Infinite Yield FE — reworked movement, fixed godmode, cleaner anticheat evasion, and more.

## Changes from base IY

- **Godmode** — complete rewrite using death detection + instant rejoin + position restore. the original clone trick was broken on most games.
- **Speed / Loopspeed** — replaced direct `WalkSpeed` manipulation with `BodyVelocity` heartbeat approach. `WalkSpeed` stays at 16 visually, actual movement velocity is pushed separately to avoid common AC flags.
- **Fly / VFly** — smoothed velocity with lerp, normalized direction vectors, force values tuned down from suspicious `9e9` to realistic levels. movement ramps in/out naturally.
- **Clickteleport** — removed. was buggy and unreliable.
- **Ungod / Unspeed** — proper cleanup commands added for all new movement systems.

## Credits

Original Infinite Yield developers:
- **Moon**
- **Zwolf**
- **Sleaze**
- **Toon**
- **Peyton** (apeyton)
- **ATP**
- **Edge**

Fork maintained by **[raidtechdev](https://github.com/raidtechdev)**

## Usage

Load via your executor. All original IY commands work. New/changed commands:

| Command | Description |
|---|---|
| `god` | Detects death, saves position, rejoins and teleports back |
| `ungod` | Stops godmode tracking |
| `speed [n]` | Sets speed. Above 24 uses BodyVelocity instead of WalkSpeed |
| `unspeed` | Resets speed and cleans up |
| `loopspeed [n]` | Persistent speed that survives respawns |
| `unloopspeed` | Stops loopspeed |

## License

Based on Infinite Yield FE. All original credit belongs to the original developers listed above.
