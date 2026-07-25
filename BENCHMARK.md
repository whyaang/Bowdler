# Bowdler ASR Benchmark Results

**Date:** 2026-07-24  
**Platform:** macOS 15.7.5, MacBook Air M4 2025 16GB
**Pipeline:** extract audio -> Silero VAD -> crop -> transcribe -> merge segments  
**Metrics:** Absolute WER/CER against Whisper Large v3 reference  
**Note:** "not chunked" = single-pass, full file at once

---

## Test Videos

| Video | Duration | Ref Words | Ref Segs | Source |
|-------|----------|-----------|----------|--------|
| vid1 | 13m47s (827s) | 1491 | 30 | [YouTube](https://www.youtube.com/watch?v=3z_eoxb13_s&t=18s) |
| vid2 | 24m52s (1492s) | 4197 | 354 | [YouTube](https://www.youtube.com/watch?v=-AcwpQsrUUs&t=1s) |
| vid3 | 45m53s (2753s) | 6626 | 603 | [YouTube](https://www.youtube.com/watch?v=iGFbNTC1NoU&t=1050s) |

---

## Results

### vid1

| Model | Words | Segs | WER | CER | Time | RTF |
|-------|-------|------|-----|-----|------|-----|
| Whisper Large v3 | 1491 | 30 | 0.00% | 0.00% | 237.8s | 0.288 |
| Whisper Medium | 1482 | 30 | 2.64% | 1.65% | 97.6s | 0.118 |
| Whisper Small | 1490 | 30 | 3.39% | 2.13% | 31.4s | 0.038 |
| Whisper Base | 1488 | 30 | 5.15% | 2.71% | 129.0s | 0.156 |
| Whisper Tiny | 1535 | 31 | 11.53% | 6.11% | 10.8s | 0.013 |
| Whisper Medium (not chunked) | 1477 | 121 | 2.56% | 1.77% | 84.7s | 0.102 |
| Whisper Large v3 (not chunked) | 1481 | 133 | 2.02% | 1.61% | 207.1s | 0.250 |
| Whisper Tiny (not chunked) | 1485 | 30 | 5.49% | 2.43% | 7.4s | 0.009 |
| Whisper Base (not chunked) | 1487 | 30 | 5.22% | 2.78% | 10.8s | 0.013 |
| Whisper Small (not chunked) | 1477 | 30 | 3.73% | 2.18% | 33.9s | 0.041 |
| Parakeet TDT 0.6B Q4_K | 1426 | 29 | 8.95% | 6.91% | 42.2s | 0.051 |
| Parakeet TDT 0.6B Q8_0 | 1434 | 29 | 7.46% | 5.72% | 38.0s | 0.046 |
| Parakeet TDT 1.1B Q4_K | 1501 | 31 | 5.02% | 3.81% | 50.4s | 0.061 |
| Parakeet TDT 1.1B Q8_0 | 1504 | 31 | 5.29% | 3.88% | 50.4s | 0.061 |
| Parakeet TDT 0.6B Q4_K (not chunked) | 1469 | 1 | 3.17% | — | 23.2s | 0.028 |
| Parakeet TDT 0.6B Q8_0 (not chunked) | 1469 | 1 | 2.90% | — | 22.2s | 0.027 |
| Parakeet TDT 1.1B Q4_K (not chunked) | 1492 | 1 | 4.99% | — | 32.2s | 0.039 |
| Parakeet TDT 1.1B Q8_0 (not chunked) | 1492 | 1 | 5.06% | — | 33.0s | 0.040 |

### vid2

| Model | Words | Segs | WER | CER | Time | RTF |
|-------|-------|------|-----|-----|------|-----|
| Whisper Large v3 | 4197 | 354 | 0.00% | 0.00% | 565.6s | 0.379 |
| Whisper Medium | 4131 | 83 | 3.43% | 2.41% | 303.5s | 0.203 |
| Whisper Small | 4138 | 83 | 3.89% | 2.52% | 113.4s | 0.076 |
| Whisper Base | 4129 | 83 | 5.29% | 3.51% | 35.1s | 0.024 |
| Whisper Tiny | 4154 | 84 | 8.53% | 5.63% | 25.4s | 0.017 |
| Whisper Medium (not chunked) | 4131 | 403 | 3.51% | 2.33% | 228.7s | 0.153 |
| Whisper Large v3 (not chunked) | 4172 | 355 | 3.63% | 2.70% | 422.0s | 0.283 |
| Whisper Tiny (not chunked) | 4144 | 83 | 7.03% | 4.29% | 36.8s | 0.025 |
| Whisper Base (not chunked) | 4129 | 83 | 5.29% | 3.51% | 50.0s | 0.034 |
| Whisper Small (not chunked) | 4138 | 83 | 3.89% | 2.52% | 148.7s | 0.100 |
| Parakeet TDT 0.6B Q4_K | 4486 | 90 | 10.29% | 7.31% | 61.2s | 0.041 |
| Parakeet TDT 0.6B Q8_0 | 4488 | 90 | 10.56% | 7.43% | 101.5s | 0.068 |
| Parakeet TDT 1.1B Q4_K | 4176 | 84 | 5.32% | 3.96% | 98.3s | 0.066 |
| Parakeet TDT 1.1B Q8_0 | 4190 | 84 | 6.72% | 4.48% | 119.4s | 0.080 |
| Parakeet TDT 0.6B Q8_0 (not chunked) | — | — | **crash** | — | — | — |
| Parakeet TDT 0.6B Q4_K (not chunked) | 4454 | 1 | 9.29% | — | 50.2s | 0.034 |
| Parakeet TDT 1.1B Q4_K (not chunked) | 4182 | 1 | 6.21% | — | 61.1s | 0.041 |
| Parakeet TDT 1.1B Q8_0 (not chunked) | 4183 | 1 | 6.74% | — | 60.0s | 0.040 |

### vid3

| Model | Words | Segs | WER | CER | Time | RTF |
|-------|-------|------|-----|-----|------|-----|
| Whisper Large v3 | 6626 | 603 | 0.00% | 0.00% | 1177.2s | 0.428 |
| Whisper Medium | 6567 | 746 | 3.96% | 2.83% | 586.8s | 0.213 |
| Whisper Small | 6590 | 688 | 4.30% | 2.89% | 210.4s | 0.076 |
| Whisper Base | 6556 | 684 | 5.53% | 3.53% | 74.1s | 0.027 |
| Whisper Tiny | 6568 | 690 | 7.49% | 4.56% | 46.4s | 0.017 |
| Whisper Tiny (not chunked) | 6561 | 688 | 7.01% | 4.30% | 31.2s | 0.011 |
| Whisper Base (not chunked) | 6529 | 669 | 5.36% | 3.38% | 50.8s | 0.018 |
| Whisper Small (not chunked) | 6524 | 644 | 4.15% | 2.96% | 154.7s | 0.056 |
| Whisper Medium (not chunked) | 6537 | 730 | 3.35% | — | 484.1s | 0.176 |
| Whisper Large v3 (not chunked) | — | — | **TIMEOUT** | — | — | — |
| Parakeet TDT 0.6B Q4_K | 6711 | 427 | 9.72% | 6.95% | 115.9s | 0.042 |
| Parakeet TDT 0.6B Q8_0 | 6707 | 436 | 9.77% | 6.88% | 133.4s | 0.048 |
| Parakeet TDT 1.1B Q4_K | 6636 | 513 | 6.01% | 4.52% | 181.8s | 0.066 |
| Parakeet TDT 1.1B Q8_0 | 6646 | 517 | 6.48% | 4.94% | 181.0s | 0.066 |
| Parakeet TDT (not chunked) | — | — | **crash (Metal)** | — | — | — |

---

## 1-Hour Video Estimates (vid3 RTF)

| Model | WER | RTF | Est. Time (1h) |
|-------|-----|-----|----------------|
| Whisper Large v3 | 0.00% | 0.428 | ~25.7 min |
| Whisper Medium | 3.96% | 0.213 | ~12.8 min |
| Whisper Small | 4.30% | 0.076 | ~4.6 min |
| Whisper Base | 5.53% | 0.027 | ~1.6 min |
| Whisper Tiny | 7.49% | 0.017 | ~1.0 min |
| Parakeet TDT 1.1B Q4_K | 6.01% | 0.066 | ~4.0 min |
| Parakeet TDT 1.1B Q8_0 | 6.48% | 0.066 | ~4.0 min |
| Parakeet TDT 0.6B Q4_K | 9.72% | 0.042 | ~2.5 min |
| Parakeet TDT 0.6B Q8_0 | 9.77% | 0.048 | ~2.9 min |
