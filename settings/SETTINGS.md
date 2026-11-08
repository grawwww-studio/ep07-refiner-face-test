# Settings

- Resolution 1080p. Base model: the int8 H3 video-and-audio build that fits a 24 GB card. At 2K on a bigger card the result may differ.
- Draft: the first 120 frames of two generated takes of one synthetic test character (a closer take and a wide take, raw 1344 x 768), one line of speech, seed 5207.
- NVIDIA refiner: Open H3 Regenerate 2K graph (`graphs/`), 3 steps, start sigma 0.909 (NVIDIA's reference) and 0.8 (the node README's fidelity setting), draft-audio mode, the latent is saved and decoded in a second step (the decode nodes are removed from the graphs here), fast VAE decode, the draft is the take's own raw video. Seeds on the closer take: 1766580932, 4103, 5207; wide take: 1766580932.
- Tutorial method (as we ran it): stage 1 is a new, smaller draft (960 x 544) made from her character sheet with the pack's example settings, then a two-stage upscale with an extracted refiner LoRA, 3 steps, start 0.909. One configuration. Seeds: closer 1766580932, 4103, 5207; wide 5207.
- SeedVR2 (closer takes): 7B, int8, one step, a wavelet colour fix on the CPU, blended half and half with a plain resize.
- Plain finish (wides): a plain resize plus a camera finish: softness, a little colour fringing, grain, a soft vignette. No AI.
- Identity scores: AuraFace and SFace, face found with YuNet, every 4th frame of the first 120 (30 frames).
- Time for the whole refiner test: 5,137 s of GPU time (about 86 GPU minutes) on one RTX 4090: the voice, the takes, and every version you see. Including the runs that picked the test character: 5,843 s (about 97 GPU minutes). No energy figure is given.
