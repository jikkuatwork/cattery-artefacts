# cattery-artefacts

Binary assets for [cattery](https://github.com/jikkuatwork/cattery) — a pure Go text-to-speech tool.

Large files are stored via **Git LFS**.

## Structure

```
models/
└── <model-name>/
    ├── model_quantized.onnx    # ONNX model
    ├── voices/
    │   ├── af_heart.bin        # Voice style vectors
    │   └── ...
    └── SHA256SUMS
```

## Models

| Model | Params | Size | License | Source |
|---|---|---|---|---|
| `kokoro-82m-v1.0` | 82M | 92MB (int8) | Apache-2.0 | [onnx-community/Kokoro-82M-v1.0-ONNX](https://huggingface.co/onnx-community/Kokoro-82M-v1.0-ONNX) |

## Voices (kokoro-82m-v1.0)

Raw float32 `[510, 256]`, ~510KB each.

**American**: `af_heart`, `af_alloy`, `af_aoede`, `af_bella`, `af_jessica`, `af_kore`, `af_nicole`, `af_nova`, `af_river`, `af_sarah`, `af_sky`, `am_adam`, `am_echo`, `am_eric`, `am_fenrir`, `am_liam`, `am_michael`, `am_onyx`, `am_puck`

**British**: `bf_alice`, `bf_emma`, `bf_isabella`, `bf_lily`, `bm_daniel`, `bm_fable`, `bm_george`, `bm_lewis`

## ORT Runtime

ONNX Runtime is downloaded directly from [Microsoft releases](https://github.com/microsoft/onnxruntime/releases) — not mirrored here.
