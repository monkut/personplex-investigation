# PersonaPlex Investigation

Investigation and setup log for [NVIDIA PersonaPlex](https://github.com/NVIDIA/personaplex).

## Project Overview
PersonaPlex is a real-time, full-duplex speech-to-speech conversational model that enables persona control through text-based role prompts and audio-based voice conditioning.

## Task Checklist
- [x] Create investigation repository.
- [ ] Investigate system requirements (GPU, RAM).
- [ ] Install dependencies (libopus-dev, moshi).
- [ ] Accept model license on HuggingFace.
- [ ] Setup HuggingFace token.
- [ ] Launch server.
- [ ] Verify Web UI access.

## Technical Details
- **Architecture**: Based on Moshi architecture and weights.
- **Model**: [nvidia/personaplex-7b-v1](https://huggingface.co/nvidia/personaplex-7b-v1)
- **License**: Code (MIT), Weights (NVIDIA Open Model license).

## Investigation Notes
### Prerequisites
- `libopus-dev` (Ubuntu/Debian)
- Python environment with `torch` and `moshi`.
- Blackwell GPUs might need specific torch/cuda versions.

### Server Setup
```bash
SSL_DIR=$(mktemp -d); python -m moshi.server --ssl "$SSL_DIR"
```
Default port: 8998.
