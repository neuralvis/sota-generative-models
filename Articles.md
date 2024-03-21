# Learning Path

## Understanding Attention 
The following ~15-30 minute videos explain conceptually how self and cross attention mechanism works in LLMs. The same mechanism is used in Stable Diffusion models to encode prompts.

1. [Transformer Neural Networks, ChatGPT's foundation, Clearly Explained](https://www.youtube.com/watch?v=zxQyTK8quyY)
2. [Illustrated Guide to Transformers Neural Network: A step by step explanation](https://www.youtube.com/watch?v=4Bdc55j80l8)

## Understanding UNets and CNNs
UNets are fundamental to diffusion models, and therefore gaining a good understanding of how they work is critical. (MADHU: More links needed here)

1. [The U-Net (actually) explained in 10 minutes](https://www.youtube.com/watch?v=NhdzGfB1q74)
2. [How Stable Diffusion Works](https://www.youtube.com/watch?v=sFztPP9qPRc): This video is slightly advanced, but it shows how attention mechanisms are combined with UNets in latent space for stable diffusion
 
## Understanding Stable Diffusion
### Conceptual Understanding 

1. *Diffusion Model Clearly Explained!* [Part 1](https://medium.com/@steinsfu/diffusion-model-clearly-explained-cd331bd41166) and [Part 2](https://medium.com/@steinsfu/stable-diffusion-clearly-explained-ed008044e07e) are good introductory articles to provide an overview of how diffusion models work.

1. [How AI Image Generators Work](https://www.youtube.com/watch?v=1CIpzeNxIhU) : Excellent introduction to the fundamental workings of UNet in the context of Stable Diffusion from [`computerphile`](https://www.youtube.com/@Computerphile).
2. [Stable Diffusion in Code](https://www.youtube.com/watch?v=-lz30by8-sU) : Introduction to basic code structure and components of Stable Diffusion from [`computerphile`](https://www.youtube.com/@Computerphile). Head over to [Google Colab](https://colab.research.google.com/drive/1roZqqhsdpCXZr8kgV_Bx_ABVBPgea3lX?usp=sharing) for code. This provides a first level down (from using `pipelines` in `diffuser` library) of running UNets iteratively. Also provides examples of how to blend between multiple prompts. 
3. [LoRA — Intuitively and Exhaustively Explained](https://medium.com/towards-data-science/lora-intuitively-and-exhaustively-explained-e944a6bff46b) This article provides a good intuitive explanation of what LoRA is and how it works. Note that LoRA is part of a family of fine-tuning approaches called “PEFT” - **Parameter Efficient Fine-Tuning**. This approach is **key to understanding how one can efficiently and quickly fine-tune a foundational diffusion model with new data**.
	- [Here is a video explainer from the LoRA authors at Microsoft](https://www.youtube.com/watch?v=DhRoTONcyZE) 
	- HuggingFace has a [PEFT library](https://github.com/huggingface/peft) to use with [diffusers](https://github.com/huggingface/diffusers).	 
4. [Classifer-free Guidance](https://sander.ai/2022/05/26/guidance.html): Once a reasonable understanding of inner workings of stable diffusion is gained from [`computerphile's`](https://www.youtube.com/@Computerphile) videos above, this article provides a mathematical intuition on how classifier-free guidance works. **Classifier-free guidance is key for how conditioning works in stable diffusion**.
5. [How I understand diffusion models (YouTube)](https://www.youtube.com/watch?v=i2qSxMVeVLI) : For a good conceptual yet mathematical understanding of how training, resolution, guidance, and distillation works in SD.


### Foundational Articles

- [Sander Dielman’s Blog](https://sander.ai/posts/): Intuitive and technical articles on Diffusion Models in general. Eg. Classifier-free guidance etc. The article [_Diffusion models are autoencoders_](https://sander.ai/2022/01/31/diffusion.html) and [_Perspectives on diffusion_](https://sander.ai/2023/07/20/perspectives.html) are excellent reads.
- Diffusion models took off like a rocket at the end of 2019, after the publication of Song & Ermon’s [seminal paper](https://arxiv.org/abs/1907.05600). There is a [blog post](http://yang-song.net/blog/2021/score/) by Song that explains the intuition.
- [What are diffusion models?](https://lilianweng.github.io/posts/2021-07-11-diffusion-models/) by Lilian Weng gives theoretical underpinnings for diffusion models.
- Studies and prior art: https://github.com/Maks-s/sd-akashic#studies-toc


### Hands-on Tutorials

1. [Stable Diffusion in Code](https://colab.research.google.com/drive/1roZqqhsdpCXZr8kgV_Bx_ABVBPgea3lX?usp=sharing): This provides a first level down (from using `pipelines` in `diffuser` library) of running UNets iteratively. Also provides examples of how to blend between multiple prompts. This is a companion code to the video [Stable Diffusion in Code](https://www.youtube.com/watch?v=-lz30by8-sU) above.
2. [Understanding Stable Diffusion from “Scratch”](https://scholar.harvard.edu/binxuw/classes/machine-learning-scratch/materials/stable-diffusion-scratch) is a bit outdated, but still a good step-by-step tutorial (co-lab notebook) to walk-through for Stable Diffusion.
3. [Introductory tutorial for Huggingface Diffuser library](https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/diffusers_intro.ipynb)  
4.  [The annotated diffusion model](https://huggingface.co/blog/annotated-diffusion) by Huggingface

The following links have not been reviewed -
1. https://course.fast.ai/Lessons/lesson9.html
2. https://www.youtube.com/watch?v=_7rMfsA24Ls&t=5s
3. https://www.youtube.com/watch?v=ZBKpAp_6TGI 

## Vision Transformers