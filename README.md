# Build-and-Learn-LLMs-from-Scratch

## Stage 1 — Core Foundations: The Transformer Architecture

**Start here.** Understand the original architecture before writing any LLM-specific code.

1. **[Attention Is All You Need: Build the Transformer from Scratch](https://www.deep-ml.com/projects/attention-is-all-you-need-build-the-transformer-from-scratch)**
   — deep-ml.com
   *The original encoder-decoder transformer. Builds attention, positional encoding, and the full architecture from the 2017 paper.*

2. **[Coding a Multimodal (Vision) Language Model from Scratch in PyTorch](https://www.youtube.com/watch?v=vAmKB7iPkWw)**
   — Umar Jamil (YouTube, ~6 hrs)
   *Dense but exceptional. Covers multi-head attention, causal masking, RoPE, GQA, KV-cache, RMSNorm. Watch after you understand basic attention.*



## Stage 2 — Build a Decoder-Only LLM (GPT-style)

**The practical core.** Decoder-only transformers are what modern LLMs actually use.

3. **[Build a Decoder-Only Transformer from Scratch](https://www.intoai.pub/p/build-a-decoder-only-transformer)**
   — Dr. Ashish Bamania (Into AI)
   *Step-by-step PyTorch build of the GPT-style decoder block: causal MHA, FFN, LayerNorm, residual connections.*

4. **[Tiny GPT from Scratch](https://www.deep-ml.com/projects/tiny-gpt-from-scratch)**
   — deep-ml.com
   *Hands-on coding challenge. Reinforces the decoder-only architecture with a minimal trainable GPT.*

5. **[Coding LLMs from the Ground Up: A Complete Course](https://magazine.sebastianraschka.com/p/coding-llms-from-the-ground-up)**
   — Sebastian Raschka (~15 hrs of video)
   *The most complete end-to-end course in the list. Tokenization → attention → architecture → pretraining → finetuning. Use as a deep companion to steps 3–4.*



## Stage 3 — Train an LLM End-to-End (Single GPU)

**Get the model actually learning.**

6. **[Build and Train an LLM from Scratch](https://www.intoai.pub/p/build-and-train-an-llm-from-scratch)**
   — Dr. Ashish Bamania (Into AI)
   *Adds the full training pipeline on top of the decoder-only transformer: dataset, tokenizer, DataLoader, optimizer, training loop, text generation.*


## Stage 4 — Scale Training to Multiple GPUs

**Move beyond a single machine.**

7. **[Distributed Data Parallel (DDP) — Theory](https://www.intoai.pub/p/distributed-data-parallel)**
   — Dr. Ashish Bamania (Into AI)
   *Explains how DDP works: model replication, data splitting, AllReduce gradient averaging. Also covers where DDP breaks down for models too large to fit on one GPU.*

8. **[Train a CNN with PyTorch DDP — Code](https://www.intoai.pub/p/train-a-cnn-with-pytorch-ddp)**
   — Dr. Ashish Bamania (Into AI)
   *Part 2 of the above. Hands-on implementation: trains a CNN on two NVIDIA T4 GPUs using PyTorch's `DistributedDataParallel` on free Kaggle GPUs.*

9. **[Distributed Training of Llama, Explained Simply](https://substack.com/@drashishbamania/p-200488145)**
   — Dr. Ashish Bamania (Into AI)
   *Zooms out to the production scale — how Meta trained Llama 3 across 16,000 GPUs using 4D parallelism (data, tensor, pipeline, context, and expert). The conceptual capstone to stages 3–4.*



## Stage 5 — Inference Optimization

**Make generation fast.**

10. **[Coding the KV Cache in LLMs](https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms)**
    — Sebastian Raschka (Ahead of AI)
    *Implement key-value caching from scratch. Explains why it gives ~5× inference speedup and the memory tradeoffs involved.*



## Stage 6 — Fine-Tuning Efficiently (LoRA / DoRA)

**Adapt a trained model without retraining everything.**

11. **[Implementing LoRA from Scratch](https://medium.com/data-science/implementing-lora-from-scratch-20f838b046f1)**
    — Martin Dittgen (TDS Archive / Medium)
    *Ground-level LoRA implementation on RoBERTa, benchmarked on GLUE and SQuAD.*

12. **[LoRA and DoRA from Scratch](https://magazine.sebastianraschka.com/p/lora-and-dora-from-scratch)**
    — Sebastian Raschka (Ahead of AI)
    *Extends LoRA with DoRA (weight-decomposed LoRA), which decouples magnitude and direction for better finetuning. Read after #11.*



## Stage 7 — Advanced Architectures

**Go beyond vanilla GPT.**

13. **[Build and Train a Mixture of Experts (MoE) LLM from Scratch](https://www.intoai.pub/p/build-and-train-a-mixture-of-experts)**
    — Dr. Ashish Bamania (Into AI)
    *Adds GQA, top-k expert routing, load balancing, and weight tying. Mirrors what Mixtral and DeepSeek use.*

14. **[Building Tiny Recursive Model from Scratch](https://moazharu.medium.com/building-tiny-recursive-model-from-scratch-when-tiny-networks-beat-giants-at-their-own-game-68d9df9e1fdb)**
    — moazharu (Medium)
    *Implements the TRM architecture — a 7M parameter model that beats 671B models on systematic reasoning by iterating with a fixed tiny network. A good mind-expander at the end.*



## Quick Reference

| Stage | Focus | # |
|-------|-------|---|
| 1 — Foundations | Transformer architecture | 1–2 |
| 2 — Decoder-only / GPT | Build a language model | 3–5 |
| 3 — Single-GPU training | Full training pipeline | 6 |
| 4 — Multi-GPU training | DDP → production scale | 7–9 |
| 5 — Inference speed | KV cache | 10 |
| 6 — Fine-tuning | LoRA, DoRA | 11–12 |
| 7 — Advanced architectures | MoE, TRM | 13–14 |


Useful resources -
- [Interview Questions - Senior LLM_MLLM Research Engineer.pdf](https://github.com/user-attachments/files/28857004/Interview.Questions.-.Senior.LLM_MLLM.Research.Engineer.pdf)
