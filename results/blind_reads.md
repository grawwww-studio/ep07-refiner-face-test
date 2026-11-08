# Blind reads: one AI model's opinion, not a measurement

Three blind reads of short clips of the synthetic test character on a 0-10 scale (0 = a real camera, 10 = obviously AI), lower = more real, margin about ±0.5. Each read was done by a fresh instance of the same AI model, not a person, shown stills and 6 fps strips with letters shuffled by script; the key was opened afterwards. It is an opinion of one AI model on one character: scores do not carry between reads (see drift), only gaps inside one read are meaningful. It is not part of the pass rule.

## Read 1: the finishes (draft, plain finish, SeedVR2 50 % + finish)
| take | draft | plain finish | SeedVR2 50 % + finish |
|---|---|---|---|
| closer | 5 | 5 | 5.5 |
| wide | 6 | 5.5 | 6 |
No finish separates from another (every gap is the 0.5 margin). Tells it listed in all six clips: evenly spaced, uniform-size freckle dots (the strongest), clean skin with little pore detail, teeth as a smooth pale bar, pearl earrings with identical catchlights, a locked frame, a few flyaways that look drawn. No shimmer seen at 6 fps; 24 fps flicker and audio not assessed. Refiners were not in this read.
Key (letter per take):
| letter | clip |
|---|---|
| C_X | draft |
| C_Y | plain finish (RAW-UP) |
| C_Z | SeedVR2 50 % + finish |
| W_X | draft |
| W_Y | SeedVR2 50 % + finish |
| W_Z | plain finish (RAW-UP) |

## Read 2 (addendum A2, written before the read): refiners and a real-camera anchor
Pre-stated: an arm more than 0.5 below the draft is called more real; all within 0.5 is called no change; an arm more than 0.5 above is called less real; the real clip's score is stated once as the anchor.
| take | draft | tutorial method | NVIDIA 0.909 | NVIDIA 0.8 | real clip (score only) |
|---|---|---|---|---|---|
| closer | 6 | 5 (seed 1766580932) | 5.5 (seed 1766580932) | 7 (seed 1766580932) | 1 |
| wide | 6.5 | 4.5 (seed 5207) | 5 (seed 1766580932) | 6.5 (seed 1766580932) | 1 |
Outcome: tutorial method more real on both takes (-1, -2); NVIDIA 0.909 more real on the wide (-1.5), inside the margin on the closer take; NVIDIA 0.8 less real on the closer take (+1), level on the wide. The real clip scored far below the draft on both takes. Limits: the real clip is low resolution and the reader says it is no fair match for sharpness; the tutorial method's face sits smaller on the wide take. The reader's notes: the tutorial method «sparse, soft» freckles that «vary in size»; NVIDIA 0.909 on the wide «almost no freckles» with an «oily sheen»; draft and NVIDIA 0.8 «lattice», «dense, evenly sized». That the better scores went to the versions that softened the freckle grid is our inference from those notes.
Key:
| letter | clip |
|---|---|
| C_P | draft |
| C_Q | tutorial method, seed 1766580932 |
| C_R | NVIDIA refiner start 0.8, seed 1766580932 |
| C_S | a low-resolution clip of a real person (score only; not shown, not shared) |
| C_T | NVIDIA refiner start 0.909, seed 1766580932 |
| W_P | tutorial method, seed 5207 |
| W_Q | draft |
| W_R | NVIDIA refiner start 0.909, seed 1766580932 |
| W_S | NVIDIA refiner start 0.8, seed 1766580932 |
| W_T | a low-resolution clip of a real person (score only; not shown, not shared) |

## Read 3 (addendum A3, written before the read): the tutorial method only
Pre-stated: on the closer take, count the tutorial method's seeds scored more than 0.5 below the draft (2 or 3 of 3 keeps the claim); on the wide take with the draft scaled down so the eye distance matches (YuNet: draft 105.93 px, tutorial method 95.68 px), more than 0.5 below keeps the wide gap.
| set | draft | tutorial seed 1766580932 | seed 4103 | seed 5207 |
|---|---|---|---|---|
| closer | 6.5 | 5 | 4 | 5.5 |
| wide, equal eye distance | 6.5 | | | 4.5 |
Outcome: 3 of 3 seeds more real (-1.5, -2.5, -1.0); the wide gap holds at equal size (-2). The seed that missed the pass rule (4103, R1 0.498) scored the most real of the three. One character, n = 3.
Key:
| letter | clip |
|---|---|
| C_F | tutorial method, seed 4103 |
| C_G | tutorial method, seed 5207 |
| C_H | draft |
| C_J | tutorial method, seed 1766580932 |
| W_F | tutorial method, seed 5207 |
| W_G | draft |

## Drift between reads
The same closer-take draft scored 5, 6 and 6.5 in the three reads, the wide draft 6, 6.5 and 6.5: absolute scores do not carry between reads, gaps inside a read do.
