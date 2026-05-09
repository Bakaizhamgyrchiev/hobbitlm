# HobbitLM 🧙‍♂️

Exploring on-device LLM inference on Apple Silicon.

## Stack

- **Runtime**: llama.cpp (via XCFramework)
- **Device**: iPhone (Apple Silicon)
- **Format**: GGUF (quantized models)

## Benchmarks

Testing on real iPhone hardware (Metal backend):

| Model | Size | Params | Quant | pp 512 (t/s) | tg 128 (t/s) |
|-------|------|--------|-------|--------------|--------------|
| SmolLM2-Instruct | 0.10 GiB | 135M | Q4_K_M | 3744 | 119 |

## Roadmap

- [x] Build llama.cpp XCFramework for iOS
- [x] Run inference on iOS Simulator
- [x] Run inference on real iPhone hardware
- [ ] Load custom GGUF model
- [ ] Build custom SwiftUI app from scratch
- [ ] Benchmark different quantizations (Q4 vs Q8 vs F16)
- [ ] Fine-tuning experiments

## Goals

Understanding the full pipeline: from PyTorch weights → GGUF conversion → 
quantization → on-device inference on Apple Silicon.