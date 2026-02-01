# Episodic Memory Benchmark for Small Language Models

This repository contains the dataset, evaluation pipeline, and analysis code for our study on episodic memory in small, locally executable language models.

## Overview

Large Language Models often exhibit strong semantic recall but struggle with episodic memory — the ability to recall events grounded in time, location, and entity context.  
This project introduces a controlled benchmark designed to isolate and evaluate episodic memory behavior under constrained inference settings.

The benchmark is inspired by the Minerva capability taxonomy and focuses on narrative-level memory rather than surface retrieval.

## Dataset

- Source narrative: 49-chapter fictional novel
- Preprocessed into episodic narrative blocks
- Each episode implicitly represents:
  - Temporal position
  - Location
  - Participating entities
  - Event content

### Question Sets

- 3 independent question sets
- 40 questions per set (120 total)
- Balanced across:
  - Atomic memory tasks
  - Composite episodic reasoning
  - Minerva capability categories

Each question is annotated with:
- Capability category
- Cue specification
- Reasoning rationale

## Evaluation Methods

We evaluate two prompting strategies:

1. **Direct Prompting**
2. **Retrieval-Augmented Generation (RAG)** using TF-IDF chunk retrieval

Evaluation metrics include:
- Token-level precision, recall, and F1
- LLM-as-a-judge correctness scoring
- Chronological awareness
- Answer length and variance analysis

## Results Summary

- Overall episodic recall remains low across all configurations
- RAG provides limited and inconsistent improvements
- Performance correlates with event density and entity recurrence
- Retrieval alone does not induce stable episodic reasoning


## Reproducibility

All experiments are designed to run under local execution constraints.
No proprietary APIs are required.

## Citation

If you use this work, please cite our paper: Coming soon...

@article{underway}
