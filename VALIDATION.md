# Validation

The notebook was rebuilt from the uploaded source notebook and reorganized into a single learning flow.

Checked areas:

- UTF-8 byte conversion
- Adjacent pair counting
- Non-overlapping BPE merging
- BPE merge-rule learning
- Vocabulary reconstruction
- Encoding
- Decoding
- Encode/decode round-trip
- GPT-2-style regex pattern
- SentencePiece BPE training configuration
- SentencePiece encode/decode round-trip

The `tiktoken` package is declared in `requirements.txt`. An execution environment needs network/package access for the installation and GPT-2 file download cells.
