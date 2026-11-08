# The rule

A refiner passes if its identity score against the character sheet (R1, mean over the clip) is within 0.028 of SeedVR2's on the same closer take, and its minimum is at least 0.37, on at least 2 of 3 seeds. Metric: AuraFace (Apache-2.0 per its repo), cosine similarity, face found with YuNet. SFace is run beside it as a cross-check and never decides.

## Where the numbers come from (honesty note)
Rule first written on another face model's scale, before an earlier test on another character. Converted to this scale from that test's frames, before this character existed. Same structure, not tuned on these results. The two constants (0.03 and 0.40 originally) became 0.028 and 0.37, rounded toward the stricter side; the conversion and its date were fixed before any frame of this test existed.

## The lines
- Closer take: SeedVR2 R1 mean 0.538 minus 0.028 = **0.510**. SeedVR2 run on the tutorial method's own small draft (first seed only): 0.572 minus 0.028 = **0.544**.
- Wide take, 1 seed per arm: SeedVR2 0.544 minus 0.028 = **0.516**. One seed never decides.
- SFace cross-check constants: 0.026 and 0.51; lines 0.684 (closer), 0.682 (against the tutorial method's own small draft), 0.672 (wide).

## Results (closer take, 3 seeds each)
- NVIDIA refiner, start 0.909: 0 of 3 seeds pass. NVIDIA refiner, start 0.8: 0 of 3. Tutorial method: 2 of 3 (seed 4103 misses at 0.498); against SeedVR2 on its own small draft the same 2 of 3.
- Wide take: start 0.909 0.322, start 0.8 0.382 (both below 0.516); tutorial method 0.570 (one seed).
- SFace gives the same verdict on every row.

## What the video's title does and does not say
«Redrew her face» is measured by R0, the score against the draft each refiner started from: the 6 NVIDIA runs (2 settings x 3 seeds, closer take) have R0 means of 0.467 to 0.726; the three plain upscalers stay at 0.893 or higher. The pass rule above measures something else: whether the face stays close to her sheet. Both are on one synthetic character, one card, the int8 build at 1080p, and the tutorial method is a different pipeline (a new, smaller clip made from her sheet, then the same refiner at start 0.909), so it is not a like-for-like setting comparison.
