# World Models

## SoTa Models
- https://github.com/dvlab-research/LISA
- DinoV2
- LLaVA - https://llava-vl.github.io/blog/
- [VILA: On Pre-training for Visual Language Models](https://github.com/NVlabs/VILA?tab=readme-ov-file) 
- https://apollo-lmms.github.io


## World Models
### Business Case
- https://a16z.com/ai-is-learning-to-build-reality/
	- https://x.com/ccamp___/status/1907810870148870588
- What are the major challenges ?
	- https://lsvp.com/stories/hello-world-models/
- Good design principles to talk about 
	- https://www.latent.space/p/claude-code?r=geyu0&utm_campaign=post&utm_medium=web


### Introductory Articles on Spatial Intelligence and World Models
- [On Spatial Intelligence for AI](https://drfeifei.substack.com/p/from-words-to-worlds-spatial-intelligence)
- [Towards Video World Models](https://www.xunhuang.me/blogs/world_model.html)
- [Beyond the Hype: How I See World Models Evolving in 2025](https://knightnemo.github.io/blog/posts/wm_2025/#33-world-models-that-integrate-multi-modal-signals)
	- The author also curates [Awesome World Models](https://github.com/knightnemo/Awesome-World-Models)

### Adjacent Articles and Papers 
- [By Jon Barron (DeepMind)](https://x.com/jon_barron/status/1909393003892097178) - good thoughts on MLPs vs Models
- https://nanonets.com/blog/bridging-images-and-text-a-survey-of-vlms/


### Seminal Papers
- https://sim-gs.github.io/ - Original Paper on WMs from Jurgen
- https://worldmodels.github.io

### SoTA Commercial World Models
- [RTFM from World Labs](https://www.worldlabs.ai/blog/rtfm)
- [Genie 3 by Google](https://deepmind.google/blog/genie-3-a-new-frontier-for-world-models/)

### SoTA Open Autoregressive Video Models
Approaches to generate Autoregressive Frames
1. Diffusion Forcing
2. Self Forcing
3. Rolling Forcing

#### Models
2. **[SkyReels-V2](https://github.com/SkyworkAI/SkyReels-V2)** - Open-source video model that uses diffusion forcing to generate continuous videos.
3. **[CausVid](https://causvid.github.io/#result)**
7. **[Self-Forcing](https://self-forcing.github.io)**
8. **[Matrix-Game 2.0](https://matrix-game-v2.github.io)**
9. **[Hunyuan Gamecraft](https://hunyuan-gamecraft.github.io)**
10. **[Tencent’s Interactive Video Generation](https://greatx3.github.io/Yan/)**
11. **[FastVideo Team’s Causal WAN](https://hao-ai-lab.github.io/blogs/fastvideo_causalwan_preview/)**

### Action Conditioned Video Models

Many of the following work use [Diffusion Forcing](https://boyuan.space/diffusion-forcing/) + [YouTube talk](https://www.youtube.com/watch?v=CNgwS8B7UvE) that combines next-token prediction and diffusion.


- [Oasis by Decarte Labs](https://oasis-model.github.io)
	- Minecraft based models. Not high quality.
- [Cosmos by nVidia](https://research.nvidia.com/labs/dir/cosmos1/)
	- Open model, code. 
	- *Only* open model for autoregressive video generation.
- [GameNGen](https://gamengen.github.io)
	- Intern project - not a high quality model
- [Lucid-v1 by unknown](https://ramimo.substack.com/p/lucid-v1-a-world-model-that-does)
	- Developer project - not a high quality model
- [GameFactory](https://yujiwen.github.io/gamefactory/) - Provides a way to train input-conditioned video generation.


