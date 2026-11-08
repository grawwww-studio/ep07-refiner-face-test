# Notices

The MIT licence in `LICENSE` covers only what we wrote for this repository: the text of `README.md`, `NOTICE.md`, `results/RULE.md` and `settings/SETTINGS.md`, the numbers in `results/`, and the graph JSON in `graphs/`. It does not cover the Grawwww name or logo (no logo file is in this repository), and it does not cover anything below.

**No model weights, no LoRA files, no frames or clips from the models, and no character sheets are in this repository.**

| Item | Where it comes from |
|---|---|
| NVIDIA Open H3 Regenerate 2K node and LoRA | NVIDIA's own project (nvlabs.github.io/Sana/Open-H3-Regenerate-2K/). The graphs in `graphs/` only name the files they load (including NVIDIA's curve file); get them from NVIDIA and read their licence. |
| MiniMax H3 base model (int8 version) | Used under the MiniMax H3 Community License Agreement. **Powered by MiniMax H3.** Get the model from its publisher. |
| The tutorial's refining method (extracted LoRA, two-stage upscale) | Described in a public tutorial; its LoRA files have no licence we could find and are not here. |
| LMS Sharp (part of NVIDIA's merged LoRA) | No licence we could find; not here. |
| SeedVR2 | Run from its public release; not here. |
| AuraFace by fal (recognition model) | Apache-2.0 per its repo (huggingface.co/fal/AuraFace-v1). Its card says it was trained on a commercial dataset; we did not audit it, and its card notes accuracy may vary by ethnicity (our character is synthetic). Not here. |
| SFace and YuNet (OpenCV Zoo) | Apache-2.0 and MIT. Used for the cross-check and for finding the face. Not here. |

All people in these tests are AI-generated and fictional. Not affiliated with NVIDIA or MiniMax.
