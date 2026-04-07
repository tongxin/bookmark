# LLMs, the architecture and building blocks


----------------------
## Attention & KV cache

- TriAttention[2026], [[project](https://weianmao.github.io/tri-attention-project-page/)][[github](https://github.com/WeianMao/triattention)][[paper](https://arxiv.org/abs/2604.04921)]
    - Key observation: Pre-ROPE Q/K values are highly concentrated. By substituting Q/Ks with their concentration centers in the original RoPE attention, a simplified formula which only depends on QK distance is derived. 


----------------------
## Training methodologies, Optimizer

Gram Newton-Schulz[2026], [[github](https://github.com/Dao-AILab/gram-newton-schulz/)]