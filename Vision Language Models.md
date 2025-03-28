# VLMs and World Models

## Introductory Material

- https://nanonets.com/blog/bridging-images-and-text-a-survey-of-vlms/

## SoTa Models
- https://github.com/dvlab-research/LISA
- DinoV2
- LLaVA - https://llava-vl.github.io/blog/
- [VILA: On Pre-training for Visual Language Models](https://github.com/NVlabs/VILA?tab=readme-ov-file) 
- https://apollo-lmms.github.io


## World Models

Many of the following work use [Diffusion Forcing](https://boyuan.space/diffusion-forcing/) that combines next-token prediction diffusion.

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

### Seminal Papers
https://worldmodels.github.io

### Genie2
- Trained with a causal mask, similar to LLMs
- Connections to diffusion forcing ?

