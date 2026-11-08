<!-- DRAFT v6 (2026-11-07), local only, not published. Proposed repo: grawwww-studio/ep07-refiner-face-test. The repo goes up only with the episode's «publica». The video slot is filled at publish time. -->
# Does an AI refiner keep her face? The settings, graphs and scores from our test

All people in these tests are AI-generated and fictional.

We ran NVIDIA's Open H3 Regenerate 2K refiner at two settings, and a popular tutorial's refining method, on one synthetic test character and compared them with plain upscalers. This repository holds what we can share: the scoring rule, the numbers (every seed), the settings, three blind reads, and the node graphs. It is a small test: one synthetic test character, AI-made footage, one card.

- Video: https://youtu.be/7bRlXvV4OAE

## What is here
| Path | What it is |
|---|---|
| `results/results_table.md` | Every arm, every seed: face-match score against her character sheet (R1) and against its own draft (R0), with AuraFace and SFace columns, and pass or fail against the rule. |
| `results/scores.jsonl` | The same numbers, one JSON line per arm and seed. |
| `results/RULE.md` | The pass rule, where its numbers come from, and what the title does and does not say. |
| `results/blind_reads.md` | Three blind reads by an AI model: scores, keys, and the addenda written before the reads. Opinion, not measurement. |
| `graphs/` | The two NVIDIA refiner graphs as ComfyUI API JSON (start sigma 0.909 and 0.8). The prompt is a placeholder. |
| `settings/SETTINGS.md` | Resolution, seeds, sigma, the tutorial method as we ran it, the finish steps, and the time. |
| `NOTICE.md` | Licences, and what is not in this repository. |

## How to read it
- Face match: AuraFace (Apache-2.0 per its repo), cosine similarity; our own test. SFace (Apache-2.0) runs beside it as a cross-check and agreed on every row. R1 is the score of the face through the clip against a character sheet; R0 is the same score against the draft the refiner started from. Higher means closer. They say whether the face stays the same person, not whether it looks real.
- The closer take has 3 seeds per refiner; the wide take has 1 seed per arm.
- The blind reads are an AI model's opinion on a 0 to 10 scale (0 = real camera, 10 = obvious AI), plus or minus 0.5, one fresh reader per read. A real-camera clip was in the second read as an anchor; only its score is given.

## Not here
No model weights, no LoRA files (ours or anyone's), no frames or clips from the models, no character sheets or prompts of our test character or of our presenter, no scoring script. The graphs name the files they load; get those from their publishers and read their licences.

## Licences
Our text and numbers here are MIT (see `LICENSE`; `NOTICE.md` says what that covers). Not affiliated with NVIDIA, MiniMax or the authors of the tutorial.
