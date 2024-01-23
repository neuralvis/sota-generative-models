# Articles

- [Sander Dielman’s Blog](https://sander.ai/posts/): Intuitive and technical articles on Diffusion Models in general. Eg. Classifier-free guidance etc. The article [_Diffusion models are autoencoders_](https://sander.ai/2022/01/31/diffusion.html) and [_Perspectives on diffusion_](https://sander.ai/2023/07/20/perspectives.html) are excellent reads.
- Diffusion models took off like a rocket at the end of 2019, after the publication of Song & Ermon’s [seminal paper](https://arxiv.org/abs/1907.05600). There is a [blog post](http://yang-song.net/blog/2021/score/) by Song that explains the intuition.
- [What are diffusion models?](https://lilianweng.github.io/posts/2021-07-11-diffusion-models/) by Lilian Weng gives theoretical underpinnings for diffusion models.
- [The annotated diffusion model](https://huggingface.co/blog/annotated-diffusion) by Huggingface
- Studies and prior art: https://github.com/Maks-s/sd-akashic#studies-toc



# Suggested Learning Path

1. [How AI Image Generators Work](https://www.youtube.com/watch?v=1CIpzeNxIhU) : Excellent introduction to the fundamental workings of UNet within Stable Diffusion from [`computerphile`](https://www.youtube.com/@Computerphile).
2. [Stable Diffusion in Code](https://www.youtube.com/watch?v=-lz30by8-sU) : Introduction to basic code structure and components of Stable Diffusion from [`computerphile`](https://www.youtube.com/@Computerphile). Head over to [Google Colab](https://colab.research.google.com/drive/1roZqqhsdpCXZr8kgV_Bx_ABVBPgea3lX?usp=sharing) for code. This provides a first level down (from using `pipelines` in `diffuser` library) of running UNets iteratively. Also provides examples of how to blend between multiple prompts. 
3. [LoRA — Intuitively and Exhaustively Explained](https://medium.com/towards-data-science/lora-intuitively-and-exhaustively-explained-e944a6bff46b) This article provides a good intuitive explanation of what LoRA is and how it works.
	4. [Here is a video explainer from the LoRA authors at Microsoft](https://www.youtube.com/watch?v=DhRoTONcyZE) 
	5. Note that LoRA is part of a family of fine-tuning approaches called “PEFT” - *Parameter Efficient Fine-Tuning*. 
	6. HuggingFace has a [PEFT library](https://github.com/huggingface/peft) to use with [diffusers](https://github.com/huggingface/diffusers).	 
4. https://www.youtube.com/watch?v=i2qSxMVeVLI : For a good conceptual yet mathematical understanding of how training, resolution, guidance, and distillation works in SD.

# Other links
1. Intro to diffusers: https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/diffusers_intro.ipynb
2. https://course.fast.ai/Lessons/lesson9.html
3. https://www.youtube.com/watch?v=_7rMfsA24Ls&t=5s
3. https://www.youtube.com/watch?v=ZBKpAp_6TGI 