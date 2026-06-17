# NL2AGBench: Benchmarking LLM Auto-Formalization for AlphaGeometry
Repo for "NL2AGBench: Benchmarking LLM Auto-Formalization for AlphaGeometry"

![Translation gap between natural-language geometry problems and AlphaGeometry's formal DSL](translation_difficulty.png)
*Figure 1: The translation gap between natural-language geometry problems and AlphaGeometry's formal DSL. While AlphaGeometry has demonstrated strong theorem-proving capabilities, the manual formalization step remains a major barrier to usability and large-scale deployment.*

## 🚧 Benchmark Construction

NL2AGBench is built from geometry problems originally formalized for AlphaGeometry:

- **Source**: The Java Geometry Expert (JGEX) repository, from which the AlphaGeometry project manually formalized 231 problems into its DSL.
- **Selection**: 48 representative problems were selected for translation diversity (circles, cyclic quadrilaterals, angle bisectors, orthocenters, circumcenters, midpoints, reflections, perpendicular constructions) and execution efficiency (excluding problems with excessive AlphaGeometry runtime).
- **Format**: Every problem pairs a natural-language statement with a verified, executable AlphaGeometry translation.

![Sample NL2AGBench problems](benchmark_image_final.png)
*Figure 2: Sample NL2AGBench problems spanning a range of geometric concepts, selected for both diversity and runtime efficiency.*
## 📊 Evaluation

We evaluate **10 state-of-the-art LLMs** (closed- and open-source, spanning multiple parameter scales).

**Table 1. Zero-Shot Model Performance**

| Closed Source | Correct | Open Source | Correct |
|---|---|---|---|
| GPT-5.4 | 75.00% | Qwen3:235B | 12.50% |
| Gemini 3.1 | 62.50% | Llama3.1:70B | 0% |
| Grok-3 | 52.08% | Llama3.2:3B | 0% |
| Sonnet 4.6 | 37.50% | Mistral:7B | 0% |
| GPT-4o:8B | 4.17% | Nemotron-3 Nano:4B | 0% |

## ☕️ Citation

```bibtex
@misc{nl2agbench2026,
      title={NL2AGBench: Benchmarking LLM Auto-Formalization for AlphaGeometry},
      author={Samuel Xiao and Judy Song and Rory Hu and Ziliang Zong},
      year={2026},
}
```

## Acknowledgements

NL2AGBench builds on the original [AlphaGeometry](https://github.com/google-deepmind/alphageometry) problem set, and draws reference translations from the [HAGeo-409](https://huggingface.co/datasets/HAGeo-IMO/HAGeo-409) benchmark.
