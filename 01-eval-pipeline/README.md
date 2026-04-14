# CoverGo — LLM Evaluation Pipeline

> Built during my CoverGo internship (08/2025 - 01/2026).
> Full implementation: https://github.com/HoTuMinh/ProductGPT-evaluation-pipeline

## Problem

CoverGo's ProductGPT (insurance AI agent) needed reliable performance measurement after each
model update. Manual QA was slow and inconsistent.

## My Approach

Built automated evaluation pipeline with 2 sub-systems:

### System 1: Benchmark-based eval

- Dataset: (Q, A, benchmark_answer) tuples
- 2 metrics: faithfulness + informativeness
- Judge: Gemini Pro
- Benchmark generation: NotebookLM

### System 2: Tester sample re-evaluation

- Input: low-rated samples from tester team
- Module: LLM-judge re-checks against source documents
- Output: verdict on whether tester rating was justified

## Key Finding

NotebookLM benchmark answers occasionally biased → augmented with **direct context-document
checking** (open-source NotebookLM alternative).

## Tech Stack

- LLM Judge: Gemini Pro
- RAG eval: NotebookLM + open-source alternative
- Metrics: faithfulness, informativeness

## Code

Full repo: https://github.com/HoTuMinh/ProductGPT-evaluation-pipeline
