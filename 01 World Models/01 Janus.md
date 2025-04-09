# 01 Janus

## Understanding vs. Generation
- Image Understanding
	- Requires high-level semantic understanding and reasoning
	- Vision encoder focuses on high-dimensional representation to capture this
- Image Generation
	- Generate local details while maintaining global consistency
	- Encoder needs low-dimensional encoding for fine-grained spatial structure/texture
- Unifying both directly will lead to conflicts and trade-offs

## Notes about the Model
1. The novelty of Janus-series of models is that they unify image understanding and image generation into a single model more tightly (using different encoders for both tasks) - resulting in better performance than other MMU and Generation models.
2. The image quality scores are limited to ~2 benchmarks (?) i think. Dall-e3, SD3-Medium, etc are a bit outdated as well. I'd be curious to see quality comparisons to SD3.5 (pro), Flux (pro), PixArt, Imagen (Google) etc.
3. Architecturally, the model uses autoregressive transformers (which is not novel - MUSE, Parti etc. use the same architecture). 
4. The [technical report](https://github.com/deepseek-ai/Janus/blob/main/janus_pro_tech_report.pdf) mentions image quality results at an output resolution of 384x384, though the model might be capable of generating higher resolution outputs. I have not been successful in generating higher resolution outputs.
5. Janus Pro demonstrates training / “data-needed” improvements.
6. Image quality is not that great, 
	7. likely because synthetic datasets have been used for pre-training - for example [Dall-e 3 high quality captions](https://huggingface.co/datasets/ProGamerGov/synthetic-dataset-1m-dalle3-high-quality-captions)
	8. Reduced the proportion of text-to-image data on Janus-pro training in Stage 3.

## What to expect next ?
The novelty is that a single model can both understand and generate images. If model architecture is improved and made performant, then we could use a single model for both pixel generation and understanding directly. You get a "world model" that both understands and generates a representation of the world either in text or images. 

Note that SoTA world models do not understand physics / light transport explicitly yet. 

What would it take for such an innovation to happen ? A partial list is below:

- Add physics, for both understanding and generation
- Improve to temporal generation (video generation)
- improve performance of model to real-time
- Add reasoning capabilities

## Links and resources
- Links to code and tech report [available here](https://github.com/deepseek-ai/Janus)
- A good tl;dr of the model is [available here](https://x.com/giffmana/status/1884011657191637126).
- Link to Huggingface discussion is [available here](https://huggingface.co/spaces/deepseek-ai/Janus-Pro-7B/discussions/5)

## Model Redux
- **Training**: Janus is trained and evaluated using [HAI-LLM](https://www.high-flyer.cn/en/blog/hai-llm/), which is a lightweight and efficient distributed training framework built on top of PyTorch. The whole training process took 7 days on a cluster of 16 nodes, each equipped with 8 Nvidia A100 (40GB) GPUs.

## Takeaways
- Focus on efficient generation of tokens - i.e. encoder/decoders for understanding and generation.
- Supporting additional modalities should be easy.
