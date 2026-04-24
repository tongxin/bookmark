# LLMs, the architecture and building blocks


----------------------
## Attention & KV cache

- TriAttention[2026], [[project](https://weianmao.github.io/tri-attention-project-page/)][[github](https://github.com/WeianMao/triattention)][[paper](https://arxiv.org/abs/2604.04921)]
    - Key observation: Pre-ROPE Q/K values are highly concentrated. By substituting Q/Ks with their concentration centers in the original RoPE attention, a simplified formula which only depends on QK distance is derived. 


----------------------
## Training methodologies, Optimizer

Gram Newton-Schulz[2026], [[github](https://github.com/Dao-AILab/gram-newton-schulz/)]
The Newton-Muon Optimizer[2026], [[paper](https://arxiv.org/pdf/2604.01472)][[slides](https://www.weijie-su.com/files/DL_Opt_muon.pdf)]

----------------------
## Training systems

- Relax: An Asynchronous Reinforcement Learning Engine for Omni-Modal Post-Training at Scale[2026], [[github](https://github.com/redai-infra/Relax)][[paper](https://arxiv.org/abs/2604.11554)]

----------------------
## VLM & Omni-modal LLMs

- vLLM Omni, [[github](https://github.com/vllm-project/vllm-omni)], [[paper](https://arxiv.org/abs/2602.02204)]