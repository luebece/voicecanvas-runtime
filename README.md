# Voicecanvas runtime files (runtime-1)

Voicecanvas downloads these files when you install a feature. Nobody else publishes these builds, so they are hosted here. Every other file comes from its original source.

| File | What it is | License |
|---|---|---|
| `audio.cpp-yue2-win-x64-cuda13.zip` | A Windows CUDA 13 build of [audio.cpp](https://github.com/0xShug0/audio.cpp) at commit `fbe3eedbf6c504e45189e2cdcf1b257740a28863`. The YuE2 runtime uses it. **This is a modified build.** It adds four patches, listed below. | Apache-2.0 (`LICENSE` is in the zip) |
| `acestep.cpp-win-x64-cuda.zip` | A Windows CUDA build of [acestep.cpp](https://github.com/ServeurpersoCom/acestep.cpp), built on 2026-06-11. It runs the ACE-Step 1.5 GGUF models. | MIT (`LICENSE` is in the zip) |

Patches in the audio.cpp build:
- `fw-cuda-kv-align-1`: aligns the CUDA KV cache.
- `score-exchange-1`: lets the YuE2 runtime take a score that is already written.
- `bounded-score-1`: keeps a score within the requested length.
- `score-identity-1`: checks that the score sung is the score given.

These files do not include any models. The models are downloaded from Hugging Face under their own licenses:
- YuE2-3B-GGUF and SheetSage2-GGUF are licensed CC BY-NC 4.0, for non-commercial use only.
- The ACE-Step 1.5 GGUF models are licensed MIT.

SHA-256:
- `audio.cpp-yue2-win-x64-cuda13.zip`: `2ef3c8fecd339e28c95c0ad9237b12f9e8ee8fce2794df59ed3d46aa74c4e7b2`
- `acestep.cpp-win-x64-cuda.zip`: `c20be84a9c8c63321f3cd3b6054c3fff36566f7fa01168e6642f30012985722d`
