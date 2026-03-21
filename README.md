# cattery-artefacts

Model and runtime artefacts for [cattery](https://github.com/jikkuatwork/cattery) — a pure Go text-to-speech tool.

Binary assets are hosted as **GitHub Release attachments**, not in git history.

## Contents (v0.1.0)

| File | Size | Description |
|---|---|---|
| `model_quantized.onnx` | 92MB | Kokoro-82M int8 ONNX model |
| `af_heart.bin` | 510KB | Default voice (American female) |
| `SHA256SUMS` | — | Checksums for all files |

## Sources

- **Model**: [onnx-community/Kokoro-82M-v1.0-ONNX](https://huggingface.co/onnx-community/Kokoro-82M-v1.0-ONNX) (Apache-2.0)
- **ORT Runtime**: Downloaded directly from [Microsoft ONNX Runtime releases](https://github.com/microsoft/onnxruntime/releases)

## Adding voices

Voice files are raw float32 arrays, shape `[510, 256]`, ~510KB each. Available voices from the Kokoro model:

**American**: `af_heart`, `af_alloy`, `af_aoede`, `af_bella`, `af_jessica`, `af_kore`, `af_nicole`, `af_nova`, `af_river`, `af_sarah`, `af_sky`, `am_adam`, `am_echo`, `am_eric`, `am_fenrir`, `am_liam`, `am_michael`, `am_onyx`, `am_puck`

**British**: `bf_alice`, `bf_emma`, `bf_isabella`, `bf_lily`, `bm_daniel`, `bm_fable`, `bm_george`, `bm_lewis`
