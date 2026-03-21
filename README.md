# cattery-artefacts

Binary assets for [cattery](https://github.com/jikkuatwork/cattery) — a pure Go text-to-speech tool.

Large files are stored via **Git LFS**. Cattery downloads directly from this repo on first run.

## What's here

- **Model** — `models/kokoro-82m-v1.0/model_quantized.onnx` (92MB)
- **Voices** — `models/kokoro-82m-v1.0/voices/*.bin` (~510KB each)
- **Checksums** — `models/kokoro-82m-v1.0/SHA256SUMS`

## What's NOT here

**ONNX Runtime** (`libonnxruntime.so`) is downloaded directly from [Microsoft's official releases](https://github.com/microsoft/onnxruntime/releases) — not mirrored here since those URLs are permanent and auth-free.

## Models

| Model | Params | Size | License | Originally from |
|---|---|---|---|---|
| `kokoro-82m-v1.0` | 82M | 92MB (int8) | Apache-2.0 | [onnx-community/Kokoro-82M-v1.0-ONNX](https://huggingface.co/onnx-community/Kokoro-82M-v1.0-ONNX) |

## Available voices (kokoro-82m-v1.0)

Raw float32 `[510, 256]`, ~510KB each.

**American**: `af_heart`, `af_alloy`, `af_aoede`, `af_bella`, `af_jessica`, `af_kore`, `af_nicole`, `af_nova`, `af_river`, `af_sarah`, `af_sky`, `am_adam`, `am_echo`, `am_eric`, `am_fenrir`, `am_liam`, `am_michael`, `am_onyx`, `am_puck`

**British**: `bf_alice`, `bf_emma`, `bf_isabella`, `bf_lily`, `bm_daniel`, `bm_fable`, `bm_george`, `bm_lewis`

## Adding a new model

```
models/
└── new-model-name/
    ├── model.onnx
    ├── voices/
    └── SHA256SUMS
```
