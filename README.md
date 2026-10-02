# Tokenization from Scratch

A practical notebook that builds a small byte-level BPE tokenizer from scratch and connects the implementation to GPT-2-style tokenization, `tiktoken`, GPT-2 tokenizer files, and SentencePiece.

## Contents

- Unicode text → UTF-8 bytes
- The 256-token base byte vocabulary
- Adjacent-pair frequency counting
- BPE merge-rule learning
- Vocabulary reconstruction
- Encoding and decoding
- Round-trip validation
- GPT-2-style regex pre-tokenization
- `tiktoken` comparison
- GPT-2 `encoder.json` and `vocab.bpe`
- `<|endoftext|>` special token
- SentencePiece BPE training

## Core idea

Byte-level BPE starts with the 256 possible byte values:

```text
0–255  → base byte vocabulary
256+   → learned BPE tokens
```

A learned token above `255` is not a new byte. It represents a reusable sequence of bytes created by merging two existing symbols.

## Run locally

```bash
pip install -r requirements.txt
```

Then open:

```text
Tokenization.ipynb
```

in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.

The notebook downloads the GPT-2 tokenizer files when that section is executed. Generated files are excluded by `.gitignore`.

## Repository structure

```text
tokenization/
├── Tokenization.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── VALIDATION.md
```

## Scope

This is an educational implementation designed to make tokenizer internals easy to inspect. It is not intended to replace optimized production tokenizers.
