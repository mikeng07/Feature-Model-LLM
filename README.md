
# Generating Realistic Feature Models with Large Language Models (LLMs)

This repository implements an approach to generate realistic feature models using **Large Language Models (LLMs)**, such as OpenAI Codex and Cohere. The goal is to create semantically coherent and syntactically valid feature model instances in the **Universal Variability Language (UVL)**, enabling advancements in variability management and software product line engineering.

---

## Overview

Feature models are widely used to represent variability in software-intensive systems. However, generating realistic feature models has been challenging due to the lack of methods that incorporate domain semantics. This project leverages LLMs to address this gap by:
- **Generating UVL models** using OpenAI Codex.
- **Validating semantic coherence** with Cohere's embedding models.
- Achieving **90% syntactic validity** for generated instances.

---

## Key Features
1. **Automatic Generation**:
   - Uses OpenAI Codex to generate new UVL feature model instances.
2. **Semantic Validation**:
   - Verifies domain coherence of generated features using Cohere embeddings and cosine similarity.
3. **Syntactic Validation**:
   - Ensures generated models conform to UVL syntax using the FLAMA framework.

---

## Architecture

The generation process consists of four main steps:
1. **Input Prompting**: Provide an existing UVL model as input.
2. **Model Inference**: Use Codex to generate new UVL instances.
3. **Syntactic Validation**: Validate the syntax of generated models using FLAMA.
4. **Semantic Validation**: Analyze domain similarity of features using Cohere embeddings.

---

## Experimental Results

- **Syntactic Validity**: 90% of generated models passed UVL syntax checks.
- **Complexity Metrics**: Generated models scored well in terms of feature count, constraints, and relationships.
- **Semantic Coherence**: Most generated features closely matched the domain of the original input model (cosine similarity scores between 0.5–0.8).

---

## Tech Stack
- **LLMs for Generation**: OpenAI Codex
- **Semantic Analysis**: Cohere API
- **Syntactic Validation**: FLAMA Framework
- **Language Representation**: Universal Variability Language (UVL)

---

## Getting Started

### Prerequisites
1. Install Python 3.x and required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Set up access to OpenAI Codex and Cohere APIs.

### Usage
1. Provide a UVL model as input.
2. Run the generation script:
   ```bash
   python generate_uvl.py --input_model example_model.uvl
   ```
3. View results in the `output/` directory.

---

## Future Work
This project lays the foundation for further research on LLMs in variability management. Future directions include:
- Improving prompt engineering techniques for better generation quality.
- Extending the approach to other domain-specific languages (DSLs).
- Exploring lightweight LLMs for broader accessibility.

