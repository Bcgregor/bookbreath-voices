---
license: cc-by-4.0
language:
- ko
library_name: coreml
pipeline_tag: text-to-speech
base_model:
- ummjevel/pocket-tts-korean-100m-distilled
- kyutai/pocket-tts
tags:
- coreml
- text-to-speech
- korean
---

# 책숨 Korean Pocket TTS (CoreML)

The Korean read-aloud model of the 책숨 (Bookbreath) e-reader app, as compiled CoreML graphs for its on-device Pocket TTS runtime.

- Base: Kyutai Pocket TTS (CC BY 4.0) and the Korean community model ummjevel/pocket-tts-korean-100m-distilled (CC BY 4.0).
- Changes: every Hangul syllable added to the tokenizer (13,964 pieces), fine-tuned on recordings of 책숨's own designed voices (no real person's voice).
- Graphs converted with FluidInference's mobius scripts; audio decoder from aufklarer/Pocket-TTS-100M-CoreML-INT8 with this model's latent statistics.
- 6 layers, cache 512, 8 flow steps, INT8 backbone, FP16 elsewhere. Same runtime contract as aufklarer/Pocket-TTS-100M-CoreML-INT8 (config.json).
