# LLaMA 3.1 Fine-Tuning

A step-by-step notebook‐based workflow to fine-tune Meta-LLaMA-3.1 (8B) using LoRA and Unsloth’s `FastLanguageModel` + TRL’s `SFTTrainer`, on a custom “test‐to‐function” dataset—and then run inference and push the new model to the Hugging Face Hub.

---

## Project Structure
```bash
.
├── finetune.ipynb # Main Colab/Notebook workflow
├── train_data.xlsx # Excel file with “instruction”, “input”, “output” columns
├── new_tests.xlsx # Excel file with inference “instruction”+“input”
├── train.jsonl # Generated JSONL formatted training data (Hugging Face dataset)
├── outputs/ # Training outputs & checkpoints
└── README.md # This file
```

---

## Requirements

- Python 3.9+
- A CUDA-compatible GPU (≥16 GB VRAM recommended)
- A valid [Hugging Face API token](https://huggingface.co/settings/tokens) with write access
