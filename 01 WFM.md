# VLMs and World Models

## World Models - Business Case
- https://a16z.com/ai-is-learning-to-build-reality/
	- https://x.com/ccamp___/status/1907810870148870588
- What are the major challenges ?
- https://lsvp.com/stories/hello-world-models/
- Good design principles to talk about 
	- https://www.latent.space/p/claude-code?r=geyu0&utm_campaign=post&utm_medium=web


## Understanding vs. Generation
- Image Understanding
	- Requires high-level semantic understanding and reasoning
	- Vision encoder focuses on high-dimensional representation to capture this
- Image Generation
	- Generate local details while maintaining global consistency
	- Encoder needs low-dimensional encoding for fine-grained spatial structure/texture
- Unifying both directly will lead to conflicts and trade-offs
- Models that combine image understanding and image generation into the same backbone (eg: Janus).
- Models that combine Image and Video Generation into the same backbone: eg. Goku by ByteDance
- Using Multimodal models for training
	- Goku uses a VLM Tarsier2
	- Janus-pro uses ?? Models for prompt alignment and training
	- Cosmos uses something ?
- Using autoregressive models

#WFM

## Introductory Material

- https://nanonets.com/blog/bridging-images-and-text-a-survey-of-vlms/

## SoTa Models
- https://github.com/dvlab-research/LISA
- DinoV2
- LLaVA - https://llava-vl.github.io/blog/
- [VILA: On Pre-training for Visual Language Models](https://github.com/NVlabs/VILA?tab=readme-ov-file) 
- https://apollo-lmms.github.io


## World Models

Many of the following work use [Diffusion Forcing](https://boyuan.space/diffusion-forcing/) + [YouTube talk](https://www.youtube.com/watch?v=CNgwS8B7UvE) that combines next-token prediction and diffusion.

- [Genie 2 from Google](https://deepmind.google/discover/blog/genie-2-a-large-scale-foundation-world-model/)
	- Highest quality model IMO. Not open, unfortunately.
- https://genesis-embodied-ai.github.io
	- Really just a physics engine with LLM.
- [Oasis by Decarte Labs](https://oasis-model.github.io)
	- Minecraft based models. Not high quality.
- [Cosmos by nVidia](https://research.nvidia.com/labs/dir/cosmos1/)
	- Open model, code. 
	- *Only* open model for autoregressive video generation.
- [causvid by Adobe + MIT](https://causvid.github.io/)
	- Good model, not open
- [GameNGen](https://gamengen.github.io)
	- Intern project - not a high quality model
- [Lucid-v1 by unknown](https://ramimo.substack.com/p/lucid-v1-a-world-model-that-does)
	- Developer project - not a high quality model
- **[SkyReels-V2](https://github.com/SkyworkAI/SkyReels-V2)** - Open-source video model that uses diffusion forcing to generate continuous videos.
- [GameFactory](https://yujiwen.github.io/gamefactory/) - Provides a way to train input-conditioned video generation.



### Seminal Papers
https://worldmodels.github.io

### Genie2
- Trained with a causal mask, similar to LLMs
- Connections to diffusion forcing ?

### Adjacent Articles and Papers 
- [By Jon Barron (DeepMind)](https://x.com/jon_barron/status/1909393003892097178) - good thoughts on MLPs vs Models
- PhysDreamer: https://physdreamer.github.io/
- PhyScene: https://physcene.github.io/
- https://sim-gs.github.io/ - Original Paper on WMs from Jurgen
- [Towards Video World Models](https://www.xunhuang.me/blogs/world_model.html)


