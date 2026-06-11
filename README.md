# Build-and-Learn-LLMs-from-Scratch

## Stage 1 — Core Foundations: The Transformer Architecture

**Start here.** Understand the original architecture before writing any LLM-specific code.

1. **[Attention Is All You Need: Build the Transformer from Scratch](https://www.deep-ml.com/projects/attention-is-all-you-need-build-the-transformer-from-scratch)**
   — deep-ml.com
   *The original encoder-decoder transformer. Builds attention, positional encoding, and the full architecture from the 2017 paper. Best starting point.*

2. **[Coding a Multimodal (Vision) Language Model from Scratch in PyTorch](https://www.youtube.com/watch?v=vAmKB7iPkWw)**
   — Umar Jamil (YouTube, ~6 hrs)
   *Dense but exceptional. Covers multi-head attention, causal masking, RoPE, GQA, KV-cache, RMSNorm, and grouped query attention — all explained with tensor diagrams. Watch after you understand basic attention.*

---

## Stage 2 — Build a Decoder-Only LLM (GPT-style)

**The practical core.** Decoder-only transformers are what modern LLMs actually use.

3. **[Build a Decoder-Only Transformer from Scratch](https://www.intoai.pub/p/build-a-decoder-only-transformer)**
   — Dr. Ashish Bamania (Into AI)
   *Step-by-step PyTorch build of the GPT-style decoder block: causal MHA, FFN, LayerNorm, residual connections.*

4. **[Tiny GPT from Scratch](https://www.deep-ml.com/projects/tiny-gpt-from-scratch)**
   — deep-ml.com
   *Hands-on coding challenge format. Reinforces the decoder-only architecture with a minimal trainable GPT.*

5. **[Coding LLMs from the Ground Up: A Complete Course](https://magazine.sebastianraschka.com/p/coding-llms-from-the-ground-up)**
   — Sebastian Raschka (~15 hrs of video)
   *The most complete end-to-end course in the list. Tokenization → attention → architecture → pretraining → finetuning for classification → instruction finetuning. Use as a deep companion to steps 3–4.*

---

## Stage 3 — Train an LLM End-to-End

**Get the model actually learning.**

6. **[Build and Train an LLM from Scratch](https://www.intoai.pub/p/build-and-train-an-llm-from-scratch)**
   — Dr. Ashish Bamania (Into AI)
   *Adds the full training pipeline on top of the decoder-only transformer built in step 3: dataset loading, tokenizer, DataLoader, optimizer, training loop, text generation.*

---

## Stage 4 — Inference Optimization

**Make generation fast.**

7. **[Coding the KV Cache in LLMs](https://magazine.sebastianraschka.com/p/coding-the-kv-cache-in-llms)**
   — Sebastian Raschka (Ahead of AI)
   *Implement key-value caching from scratch, understand why it gives ~5× inference speedup, and learn the memory tradeoffs. Requires solid understanding of the attention mechanism.*

---

## Stage 5 — Fine-Tuning Efficiently (LoRA / DoRA)

**Adapt a trained model without retraining everything.**

8. **[Implementing LoRA from Scratch](https://medium.com/data-science/implementing-lora-from-scratch-20f838b046f1)**
   — Martin Dittgen (TDS Archive / Medium)
   *Ground-level LoRA implementation on RoBERTa, benchmarked on GLUE and SQuAD. Good first pass at the concept with full from-scratch code.*

9. **[LoRA and DoRA from Scratch](https://magazine.sebastianraschka.com/p/lora-and-dora-from-scratch)**
   — Sebastian Raschka (Ahead of AI)
   *Follow-on to #8. Adds DoRA (weight-decomposed LoRA), which decouples magnitude and direction for better finetuning performance. Read after #8.*

---

## Stage 6 — Advanced Architectures

**Go beyond vanilla GPT.**

10. **[Build and Train a Mixture of Experts (MoE) LLM from Scratch](https://www.intoai.pub/p/build-and-train-a-mixture-of-experts)**
    — Dr. Ashish Bamania (Into AI)
    *Adds Grouped Query Attention (GQA), top-k expert routing, load balancing, and weight tying on top of the decoder-only foundation. Mirrors what Mixtral and DeepSeek use.*

11. **[Building Tiny Recursive Model from Scratch](https://moazharu.medium.com/building-tiny-recursive-model-from-scratch-when-tiny-networks-beat-giants-at-their-own-game-68d9df9e1fdb)**
    — moazharu (Medium)
    *Diverges from the standard transformer path. Implements the TRM architecture — a 7M parameter model that beats 671B models on systematic reasoning by iterating with a fixed tiny network rather than scaling. A good mind-expander at the end.*

---

## Quick Reference

| Stage | Focus | Resources |
|-------|-------|-----------|
| 1 | Transformer fundamentals | deep-ml Transformer, Umar Jamil video |
| 2 | Decoder-only / GPT | deep-ml Tiny GPT, Bamania decoder, Raschka course |
| 3 | Training pipeline | Bamania train LLM |
| 4 | Inference speed | Raschka KV cache |
| 5 | Fine-tuning | Dittgen LoRA, Raschka LoRA+DoRA |
| 6 | Advanced architectures | Bamania MoE, moazharu TRM |
