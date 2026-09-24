# Bonsai 2 demos

Olympiad-level evaluations of [Bonsai 2 27B](https://huggingface.co/prism-ml/Ternary-Bonsai-2-27B-gguf) alongside two other open-weight models, Qwen3.8 27B and Gemma 4 12B QAT. Every model ran on the same [Prism llama.cpp](https://github.com/PrismML-Eng/llama.cpp/releases/tag/prism-b10709-9a9394a) runtime with pinned weights, on one NVIDIA H200 GPU per run. Each folder includes the exact settings and code to reproduce its runs.

| Folder | Benchmark | What's inside |
|---|---|---|
| [`imo2026/`](imo2026) | IMO 2026, six proof problems | Final answers from each model at a 131k-token thinking budget, plus a script to rerun any problem |

## Headline results

**IMO 2026**, out of 42, one attempt per problem at a 131k-token thinking budget:

| Model | Weights | Score | P1 | P2 | P3 | P4 | P5 | P6 |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| Qwen3.8 27B | BF16, 53.8 GB | 22 | 7 | 0 | 1 | 7 | 7 | 0 |
| Bonsai 2 27B | PQ2_0, 7.2 GB | 21 | 7 | 0 | 0 | 7 | 7 | 0 |
| Gemma 4 12B QAT | Q4_0, 7.0 GB | 7 | 7 | 0 | 0 | 0 | 0 | 0 |

Scores are our own grades of the final answers against [Evan Chen's IMO 2026 solution notes](https://web.evanchen.cc/exams/IMO-2026-notes.pdf), not official marks; the official marking schemes are not public. See [`imo2026/`](imo2026) for the answers and how to reproduce them.

## License

Repository contents are released under [CC BY 4.0](LICENSE). Each model is under its own license.
