# Protein-Generation-Bio-Gpt

# 🧬 ProtGPT2 + LoRA Protein Generator & Evaluator

This project demonstrates **protein sequence generation and evaluation** using **ProtGPT2** with **LoRA fine-tuning**, combined with interactive visualization and evaluation of generated protein sequences. The pipeline also includes **training loss tracking** and multi-property analysis plots.

---

## Features

1. **ProtGPT2 Base Model**
   - Uses [nferruz/ProtGPT2](https://huggingface.co/nferruz/ProtGPT2) for protein sequence generation.
   - Supports causal language modeling on protein sequences.

2. **LoRA Fine-Tuning**
   - Low-Rank Adaptation (LoRA) applied for efficient fine-tuning.
   - Reduces trainable parameters while adapting the model to custom sequences.

3. **Custom Protein Dataset**
   - Accepts a local list of protein sequences for training.
   - Tokenizes sequences for causal LM training.

4. **Protein Property Evaluation**
   - Computes molecular weight, instability index, GRAVY, aromaticity, and sequence length.
   - Evaluates generated sequences using `Bio.SeqUtils.ProtParam.ProteinAnalysis`.

5. **Visualization**
   - **Histograms & KDEs** for protein properties.
   - **Scatter plots** of property relationships.
   - **Violin plots** for distribution analysis.
   - **Pairplot** for pairwise property visualization.
   - **Correlation heatmap** for feature correlations.
   - **CDF plots** for cumulative distribution functions.
   - **Training loss plots** to monitor model convergence.

6. **Interactive UI (Gradio)**
   - Input prompt for protein generation.
   - Adjustable parameters: max length, temperature, top-p sampling.
   - Displays generated sequences, property evaluations, and plots.

---

## Installation

```bash
pip install transformers peft accelerate datasets gradio biopython matplotlib seaborn
