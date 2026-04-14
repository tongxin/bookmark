# NV AI projects


-------------------
## LLMs, VLMs pre-training, post-training

- Megatron, https://github.com/NVIDIA/Megatron-LM
    - Includes MegatronLM and Megatron Core
- Nemo Megatron Bridge, https://github.com/NVIDIA-NeMo/Megatron-Bridge
    - provides pretraining, SFT and LoRA for popular LLM and VLM models.
- Emerging Optimizers, https://github.com/NVIDIA-NeMo/Emerging-Optimizers
- Nemo RL, https://github.com/NVIDIA-NeMo/RL
- Nemo Gym, https://github.com/NVIDIA-NeMo/Gym
- Cosmos-RL, https://github.com/nvidia-cosmos/cosmos-rl

-------------------
## GenAI & World Model

- Cosmos-Predict2.5, https://github.com/nvidia-cosmos/cosmos-predict2.5, [Paper](https://arxiv.org/abs/2511.00062)

- DreamDojo, https://github.com/NVIDIA/DreamDojo, [Paper](https://arxiv.org/abs/2602.06949)
    - Presents with 44k hours of egocentric video dataset
    - An interactive world model trained on large scale human centric videos
    - Builds on Cosmos-Predict2.5


-------------------
## Physical AI and Robotics

- Isaac GR00T, https://github.com/NVIDIA/Isaac-GR00T, [Project](https://developer.nvidia.com/isaac/gr00t), [Paper](https://arxiv.org/abs/2503.14734)
    - A humanoid VLA foundation model that integrates VLM based reasoning and DiT based action modules

- Cosmos-Policy, https://github.com/NVlabs/cosmos-policy, [Project](https://research.nvidia.com/labs/dir/cosmos-policy/), [Paper](https://arxiv.org/abs/2601.16163)
    - Downstream robot policy models that consume world model outputs to generate executions for sim/real robots.
    - Built with Cosmos Predict/Transfer/Reason as a policy model component.
    - Uses diffusion to generate actions.

- SAGE, https://github.com/NVlabs/sage
    - Comes with a 10K indoor scene dataset
    - Generates 3D scenes for training embodied AI

- DreamZero, [[project](https://dreamzero0.github.io/)], [[github](https://github.com/dreamzero0/dreamzero)], [[paper](https://arxiv.org/abs/2602.15922)]


-------------------

## AI4S

- PhysicsNemo, https://github.com/NVIDIA/physicsnemo
