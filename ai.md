# AI research works by topics


-----------------
## GenAI & World model & interactive AI

- Classifier free Diffusion Guidance[2021], [[paper](https://arxiv.org/abs/2207.12598)]
    - Learns to predict the noise given the condition and without condition.
    - The difference of the two predicted errors represents the direction towards satisfying the condition.
    - The uses a guiding scale w to interpolate/extrapolate the noise prediction along this direction.
    - Small w forces weak guidance, large w strong guidance.


- Genie[2024], [[Project](https://sites.google.com/view/genie-2024/home)][[Paper](https://arxiv.org/abs/2402.15391)]
    - Learns latent actions that generalize to diverse environments.
    - Self supervised trained on video only data.
    - Architecture
        - Parallel video tokenizer and latent action model followed by a dynamics model.
        - Uses ST-transformer for reduced attention complexity.
        - L spatiotemporal attention layers, each includes
            - a spatial layer: self attention, 1 x H x W tokens, within each time step
            - a temporal layer: causal attention, T x 1 x 1 tokens, across T time steps
            - a ffn layer
        - Video tokenizer: VQ-VAE on entire video sequence
            - encoder: input past frames and output the next latent, 1:T x H x W x C -> 1 x D
            - decoder: input past latents and output the next frame, 1:T x D -> 1 x H x W x C
        - Latent action model (LAM):
            - encoder: input past frames and output next action, 1:T x H x W x C -> 1 x K
            - decoder: input past frames and actions, output next frame, 1:T x H x W x C, 1:T x K -> 1 x H x W x C
            - note, apart from the codebook, the decoder is not used at inference time.
        - VQ-VAE training
            - Limit latent action's VQ codebook size to a small number, like 8.
            - Latent actions' sparsity enforces the learner to capture the most meaningful changes from past to future frames.
            - uses the above ST-transformer for LAM training.
        - Dynamics model
            - decoder only MaskedGiT
            - input past video latents and stopgrad actions, predict next frame tokens.
            - to train:
                - apply cross entroy loss between all predicted frame tokens and ground truth tokens.
                - apply random masks on input tokens.

- Diffusion Forcing, [[project](https://www.boyuan.space/diffusion-forcing/)], [[github](https://github.com/buoyancy99/diffusion-forcing)], [[paper](https://arxiv.org/abs/2407.01392)]


- Wan, [[github](https://github.com/Wan-Video/Wan2.2)], [[paper](https://arxiv.org/abs/2503.20314)]

- Magi-1, [[project](https://magi-1.ai/)], [[github](https://github.com/SandAI-org/MAGI-1)], [[paper](https://arxiv.org/abs/2505.13211)]
    - Learns to denoise per video chunk noise, using flow-matching to train.
    - Uses a transformer VAE for image encoding/decoding.

- AdaWorld[ICML'2025], [[Project](https://adaptable-world-model.github.io/)][[Code](https://github.com/Little-Podi/AdaWorld)][[Paper](https://arxiv.org/abs/2503.18938)]
    - Learns a latent action VAE, improving scene transfer results.
    - Self-supervised trained on large scale videos.
    - Architecture
        - Uses the predicted latent actions and a denoiser network to iteratively refine next frame generation.

- Hunyuan WorldPlay, [[github](https://github.com/Tencent-Hunyuan/HY-WorldPlay)], [[paper](https://arxiv.org/abs/2512.14614), [paper](https://arxiv.org/abs/2602.09022)]

- GigaWorld Policy, [[github](https://github.com/open-gigaai/giga-world-policy)], [[paper](https://arxiv.org/abs/2603.17240v1)]


-----------------
## Physical AI

- π0.7[2026], [[blog](https://www.pi.website/blog/pi07)], [[paper](https://www.pi.website/download/pi07.pdf)]

- [[blog](https://www.pi.website/blog/pistar06)], [[paper](https://www.pi.website/download/pistar06.pdf)]

- π0.5[2025], [[blog](https://www.pi.website/blog/pi05)], [[paper](https://www.pi.website/download/pi05.pdf)]

- RDT-1B[2025], [[blog](https://rdt-robotics.github.io/rdt-robotics/)], [[paper](https://arxiv.org/abs/2410.07864)]

- RDT2[2026], [[project](https://rdt-robotics.github.io/rdt2/)], [[paper](https://arxiv.org/abs/2602.03310)]
    - A foundation model that can achieve zero-shot deployment on unseen embodiments
    - 10,000+ hours of real world home and office scene videos produced on 100+ UMIs

- Generalist GEN-0[2025][[blog](https://generalistai.com/blog/nov-04-2025-GEN-0)], GEN-1[2026][[blog](https://generalistai.com/blog/apr-02-2026-GEN-1)]
    - Embodied Foundation Models That Scale with Physical Interaction

- UMI gripper[2024], [[project](https://umi-gripper.github.io/)], [[paper](https://arxiv.org/abs/2402.10329)]

- Diffusion Policy[2023], [[github](https://github.com/real-stanford/diffusion_policy)], [[paper](https://arxiv.org/abs/2303.04137)]

- CoT-VLA[2025], [[project](https://cot-vla.github.io/)], [[paper](https://arxiv.org/abs/2503.22020)]

-----------------

## Spatial intelligence

- On Evaluation of Embodied Navigation Agents[2018], [[paper](https://arxiv.org/abstract/1807.06757)]
    - Proposes a measure to evaluate successfulness of agent navigation. Key points:
    - Agents must signal 'Done' to indicate they are aware of their status
    - Navigation performance is a weighed sum of successfulness over trials where weights are inverse normalized path length.
    - Jitendra Malik proposes to use inverse normalized time instead of path length for weights in his X tweets.


-----------------
## AI in a Science Perspective

- Artificial Intelligence and the Structure of Mathematics[2026], [[paper](https://arxiv.org/abs/2604.06107v1)]
    - Hypergraphs and universal properties of mathematics
