# OnnxGo Models

Browser-ready [KataGo](https://github.com/lightvector/KataGo) networks in ONNX format, used by **OnnxGo** —
a web app that runs Go AI suggestions entirely on the user's own device.

This repository only hosts model files (as GitHub Release assets) and their license. It contains no application code.

## Models

| Release | File | Size | SHA-256 |
|---------|------|------|---------|
| [`b18c384nbt-lite-v1`](https://github.com/aerinSie/OnnxGo-models/releases/tag/b18c384nbt-lite-v1) | `katago-b18c384nbt-lite.uint8.onnx` | 30.5 MB | `f41050b8e820b60bc06262faddc0d2645d1ec220180e23559620815fe7a3ac27` |

- **Source network:** `kata1-b18c384nbt-s9996604416-d4316597426`
  (official PyTorch checkpoint from <https://katagotraining.org/networks/kata1/>)
- **Conversion:** exported to ONNX (opset 17) and dynamically quantized to UINT8 weights using
  [kaya-go/katago-onnx](https://github.com/kaya-go/katago-onnx) as a tool. No code from that project is included here.
- **Inputs:** `bin_input [N, 22, 19, 19]`, `global_input [N, 19]` (KataGo V7 features)
- **Outputs:** `policy`, `value`, `miscvalue`, `moremiscvalue`, `ownership`, `scoring`, `futurepos`, `seki`, `scorebelief`

## License

The network weights are distributed under the **KataGo Neural Network License** (MIT-style).
See [LICENSE-KataGo-network.txt](LICENSE-KataGo-network.txt) — the same notice is attached to every release.
