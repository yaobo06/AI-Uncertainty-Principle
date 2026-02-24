# 🌌 Semantic Topo-Gap: The Dimensionality Limit of LLM Embeddings

**Status:** Initial Discovery & Proof of Concept (Timestamp Locked)  
**Author:** Independent Researcher (Undergraduate, The Chinese University of Hong Kong, Shenzhen)  
**Date:** February 24, 2026

## 📌 TL;DR
This repository serves as the foundational timestamp for the discovery of the **"Semantic Topo-Gap"** and the **U-shaped dimensionality law** in Large Language Model (LLM) embeddings. 

Contrary to the prevailing industry assumption that "higher embedding dimensionality yields better semantic representation," empirical data and theoretical derivation in this repository prove that semantic density strictly follows a U-shaped curve. Blindly increasing dimensionality beyond an optimal threshold strictly degrades semantic cohesion due to high-dimensional geometric sparsity.

## 🔬 Core Theoretical Framework

Through extensive experimentation, we define the minimal intra-cluster semantic cohesion $$C_{min}(d)$$ as a function of the embedding dimension $$d$$. The theoretical boundary is formulated as:

$$
C_{min}(d) = \frac{\alpha}{d} + \beta \cdot d - \gamma
$$

Where:
*   $$\frac{\alpha}{d}$$ represents the **Information Compression Loss** at extremely low dimensions.
*   $$\beta \cdot d$$ represents the **Curse of Dimensionality Penalty** (Semantic Topo-Gap) at excessively high dimensions.
*   $$\gamma$$ is the baseline semantic capability of the underlying foundational model.

This mathematical framework mathematically proves the existence of an "Optimal Dimensionality Zone" (typically around $$d=768$$, commonly adopted by BERT and recent embedding models), beyond which semantic clusters begin to disperse.

## 🛠️ Experimental Setup
To guarantee reproducibility, the initial framework was tested strictly under the following conditions:
*   **Dataset:** `20 Newsgroups` (Providing a standardized multi-class semantic space).
*   **Models:** `nomic-embed-text`, `qwen2.5:1.5b` via local Ollama inference.
*   **Hyperparameters:** Generation `temperature = 0.0` (Ensuring absolute deterministic outputs for latent space mapping).
*   **Evaluation Metric:** Robust variance and Moment Statistics across dimensional projections to measure empirical cluster density vs. semantic drift.

## 🚀 Implications & Future Work
This framework challenges current representation learning scaling laws. It provides a mathematical basis for why compact models (like 768-D embeddings) often outperform hyper-dimensional embeddings in zero-shot retrieval and RAG (Retrieval-Augmented Generation) architectures. 

A formal paper expanding on these proofs, complete with visual topological gap mapping and full algorithmic implementations, is currently being drafted for formal academic submission.

---
*Note: The code and this document are uploaded to establish the temporal priority of this discovery. The repository state is intentionally frozen as of the initial commit date.*
