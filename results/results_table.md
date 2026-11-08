# Results: every arm, every seed

Identity score of the face through the clip, mean over every 4th frame of the first 120 (30 frames), face found with YuNet. **AuraFace** (shown metric) and **SFace** (cross-check), cosine similarity, higher = closer.
R1 = against her character sheet. R0 = against the draft the arm started from. Closer take = 3 seeds per refiner; wide take = 1 seed per arm. One synthetic test character, AI-made footage.

| take | arm | seed | AuraFace R1 mean | R1 min | R0 mean | R0 min | SFace R1 mean | SFace R0 mean | passes the rule |
|---|---|---|---|---|---|---|---|---|---|
| closer | draft | 5207 | 0.565 | 0.481 | 1.000 | 1.000 | 0.714 | 1.000 |  |
| closer | AI upscaler (ESRGAN x4) | 5207 | 0.568 | 0.487 | 0.932 | 0.853 | 0.720 | 0.967 |  |
| closer | SeedVR2 | 5207 | 0.538 | 0.446 | 0.893 | 0.818 | 0.710 | 0.937 |  |
| closer | plain finish (resize + camera finish) | 5207 | 0.560 | 0.498 | 0.970 | 0.925 | 0.716 | 0.987 |  |
| closer | SeedVR2 50 % + finish | 5207 | 0.548 | 0.469 | 0.950 | 0.897 | 0.716 | 0.973 |  |
| closer | NVIDIA refiner, start 0.909 | 1766580932 | 0.417 | 0.354 | 0.610 | 0.439 | 0.575 | 0.645 | no |
| closer | NVIDIA refiner, start 0.909 | 4103 | 0.287 | 0.210 | 0.467 | 0.320 | 0.424 | 0.572 | no |
| closer | NVIDIA refiner, start 0.909 | 5207 | 0.343 | 0.285 | 0.552 | 0.443 | 0.435 | 0.610 | no |
| closer | NVIDIA refiner, start 0.8 | 1766580932 | 0.460 | 0.400 | 0.726 | 0.664 | 0.644 | 0.793 | no |
| closer | NVIDIA refiner, start 0.8 | 4103 | 0.400 | 0.323 | 0.622 | 0.469 | 0.557 | 0.731 | no |
| closer | NVIDIA refiner, start 0.8 | 5207 | 0.393 | 0.338 | 0.669 | 0.546 | 0.519 | 0.768 | no |
| closer | tutorial method | 1766580932 | 0.585 | 0.534 | 0.733 | 0.636 | 0.697 | 0.790 | yes |
| closer | tutorial method | 4103 | 0.498 | 0.420 | 0.686 | 0.642 | 0.606 | 0.777 | no |
| closer | tutorial method | 5207 | 0.564 | 0.496 | 0.695 | 0.592 | 0.711 | 0.774 | yes |
| closer | SeedVR2 on the tutorial method's own small draft (first seed only) | 1766580932 | 0.572 | 0.500 | 0.907 | 0.871 | 0.708 | 0.943 |  |
| wide | draft | 5207 | 0.532 | 0.463 | 1.000 | 1.000 | 0.710 | 1.000 |  |
| wide | AI upscaler (ESRGAN x4) | 5207 | 0.540 | 0.460 | 0.933 | 0.903 | 0.704 | 0.968 |  |
| wide | SeedVR2 | 5207 | 0.544 | 0.464 | 0.896 | 0.845 | 0.698 | 0.935 |  |
| wide | plain finish (resize + camera finish) | 5207 | 0.532 | 0.478 | 0.975 | 0.944 | 0.711 | 0.989 |  |
| wide | SeedVR2 50 % + finish | 5207 | 0.533 | 0.471 | 0.952 | 0.925 | 0.707 | 0.974 |  |
| wide | NVIDIA refiner, start 0.909 | 1766580932 | 0.322 | 0.273 | 0.410 | 0.345 | 0.359 | 0.509 | no |
| wide | NVIDIA refiner, start 0.8 | 1766580932 | 0.382 | 0.326 | 0.584 | 0.460 | 0.483 | 0.663 | no |
| wide | tutorial method | 5207 | 0.570 | 0.529 | 0.688 | 0.634 | 0.707 | 0.793 | yes |

R0 for the tutorial method is against its own first, smaller stage (it makes a new clip, so its R0 is not comparable with an upscaler's). The wide-take row for the tutorial method is a single seed and never decides alone.

## Eye distance in the raw frames (the only face-size figure shared)

Detector YuNet, 17 frames each, raw 1344 x 768 frames: closer take 98.99 px, wide take 75.41 px, ratio 1.31.
