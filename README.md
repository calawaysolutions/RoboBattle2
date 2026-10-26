# RoboBattle Direct

The no-cards sibling of [RoboBattle](https://github.com/calawaysolutions/RoboBattle): the same
shredding arena floor, laser and AI rivals, but you drive the robot directly with the arrow keys and
use abilities on cooldowns. No cards, no queue, no beat.

Two codebases, one world. Playing both back to back shows what the card queue adds to the game.

| Path | What it is |
| --- | --- |
| `microstudio/engine/` | The Chispita engine (microScript). Paste into the microStudio project once. |
| `microstudio/game/` | The game's source files, one per microStudio source file. See its README for install and controls. |

microStudio has no git integration; this repo is the source of truth and the editor is where it runs.
Copy a file in, or copy it back out, with select all + paste. Keep file names identical on both sides.
