# CoverGo Internship — LLM Evaluation & Document Security

08/2025 - 01/2026 | AI Team @ CoverGo Insurtech

## Overview

During my CoverGo internship, I focused on:

1. **Automated evaluation pipelines** for ProductGPT (insurance AI agent)
2. **Forged document detection** research for KYC security

## Projects

### [01-eval-pipeline/](./01-eval-pipeline/)
LLM-as-Judge evaluation framework with 2 sub-systems.

**System 1:** Benchmark-based eval (faithfulness + informativeness, Gemini judge, NotebookLM benchmark generation)  
**System 2:** Tester sample re-evaluation module

**Key finding:** NotebookLM benchmarks occasionally biased → augmented with direct context-document checking.

**Full implementation:** [github.com/HoTuMinh/ProductGPT-evaluation-pipeline](https://github.com/HoTuMinh/ProductGPT-evaluation-pipeline)

[→ Project details](./01-eval-pipeline/README.md)

### [02-forged-doc/](./02-forged-doc/)
Survey of 3 forgery detection approaches on CASIA v2:

1. TruFor (vision-only forensics)
2. 0-shot VLM (Groq llama-3.2-90b-vision)
3. RAG-based hybrid (vision + LLM logic check) — proposed approach

[→ Survey notebook](./02-forged-doc/forged_doc_survey.ipynb)

## Author

**Ho Tu Minh** | Final-year AI undergrad @ UET-VNU  
htm93313@gmail.com | [LinkedIn](https://www.linkedin.com/in/ho-tu-minh/)
