# 06-forged-doc/survey — Forged Document Detection Survey

Comparative survey of three forgery-detection approaches on a CASIA v2 tampered image.

## Notebook: `forged_doc_survey.ipynb`

| Section | Approach | Status |
|---|---|---|
| 1 | TruFor (mock pipeline) | Mock — real checkpoint at https://github.com/grip-unina/TruFor |
| 2 | VLM 0-shot (Groq llama-3.2-90b-vision) | Live API call |
| 3 | RAG-based (literature review + architecture) | Discussion only |

## How to run

```bash
cd 06-forged-doc/survey
pip install jupyter
jupyter notebook forged_doc_survey.ipynb
```

Requires `GROQ_API_KEY` in `.env` (two levels up) for Section 2.
If key is absent, Section 2 falls back to a mock result.

## Key findings

- **TruFor** excels at pixel-level anomaly localization but is blind to semantic forgeries.
- **VLM 0-shot** provides semantic reasoning with zero training but risks hallucination.
- **RAG-based** is most promising for document-domain forgeries where semantic consistency
  matters more than pixel statistics.

## Scope & Limitations

- TruFor section uses a **mock** pipeline — heatmap is synthetic, not from the real model.
- VLM results are non-deterministic; re-running may give different verdicts.
- No quantitative benchmark is run here; this is a qualitative survey.
- Dataset: single sample from CASIA v2; results not generalizable.
