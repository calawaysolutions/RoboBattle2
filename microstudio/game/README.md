# RoboBattle Direct — the no-cards version (microStudio + Chispita)

Same shredding floor, same laser, same AI rivals as RoboBattle, but you drive the robot directly.
No cards, no queue, no beat. It exists to show what the cards add by taking them away, and as a
second style of the same game for the class.

## Install

1. Open a microStudio project (or make a new one). Paste the nine `chispita_*` files from
   `microstudio/engine/` in as source files with the same names.
2. In the Code tab add seven new source files with these exact names and paste each `.txt` in:
   - `rb_config` (every tunable)
   - `rb_floor`
   - `rb_cards` (abilities, movement, laser)
   - `rb_bot`
   - `rb_tick`
   - `rb_hud`
   - `rb_ai`
3. Replace the project's `main` with `main.txt`.
4. Options tab: Landscape, 16:9.
5. Run. Click inside the preview once so it has keyboard focus.

## Controls

| Key | Does |
| --- | --- |
| Arrows / WASD | Move one plate in that direction and face it. Hold to keep moving (one plate per 0.35 s) |
| Space | Laser along your facing, 6 plates, 1.5 s cooldown. 3 hits cost a life |
| Q | Jump: hop 2 plates forward over anything |
| F | Decay: the next 10 plates you step on fall 5 ticks later (your own trail can get you) |
| E | Patch: restore the void plate in front of you for 8 ticks |
| R | Reinforce: your plate and its neighbors cannot fall for 10 ticks |
| Enter | Restart after the match ends |
| F1 | Chispita debug panel |

Abilities share an 8 s cooldown each; click their boxes in the HUD to use them with the mouse.

## Rules

- The floor shreds on its own timer (every 2 s), never splitting, paced to finish in about 5 minutes.
  Amber 3·2·1 plates are the next to fall.
- Falling costs a life. Three laser hits cost a life. Three lives. Last robot standing wins.
- Robots block each other; there is no pushing.

## Tuning

Everything is in `rb_config`: move rate, laser and ability cooldowns, floor tick, lives, hits per
life, arena size, shred pacing, ability numbers, AI presets and spawns.

## If something breaks

Open the microStudio console. microScript never stops on an error, so a typo shows up as a
Chispita warning or a feature that silently does nothing. F1 opens the debug panel.
