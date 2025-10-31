

{{TOC}}



# Encoders-Decoders
## Conceptual Understanding 
- [Video explaining VQ-VAE](https://www.youtube.com/watch?v=updRZIvaqCY)

## Deeper Understanding
- [Understanding VQ-VAE](https://mlberkeley.substack.com/p/vq-vae)
- [Dall-E is based on VQ-VAE](https://mlberkeley.substack.com/p/dalle2)
- [Tutorial - What is a variational autoencoder?](https://jaan.io/what-is-variational-autoencoder-vae-tutorial/)
- [Variational Autoencoders are Beautiful](https://www.compthree.com/blog/autoencoder/)
- Seminal Paper that introduced VQ-VAE: https://arxiv.org/abs/1711.00937

# Latent Spaces
- The problem of *[entanglement in image synthesis](https://blog.metaphysic.ai/entanglement-in-image-synthesis/)*
	- [What is the latent space of an image synthesis system ?](https://blog.metaphysic.ai/what-is-the-latent-space-of-an-image-synthesis-system/)

# Attention 
## Conceptual Understanding
The following ~15-30 minute videos explain conceptually how self and cross attention mechanism works in LLMs. The same mechanism is used in Stable Diffusion models to encode prompts, and in the UNet Layers.

1. [Transformer Neural Networks, ChatGPT's foundation, Clearly Explained](https://www.youtube.com/watch?v=zxQyTK8quyY):  This is a first pass overview of attention mechanics
2. [Visualizing Attention](https://www.youtube.com/watch?v=eMlx5fFNoYc) by 3Blue1Brown has an excellent explanation of both multi-head attention and of cross-attention mechanism
2. [Illustrated Guide to Transformers Neural Network: A step by step explanation](https://www.youtube.com/watch?v=4Bdc55j80l8)
3. [Transformers explained visually](https://medium.com/towards-data-science/transformers-explained-visually-part-1-overview-of-functionality-95a6dd460452)
	4. Explains how an ecoder-decoder attention works in relation to other parts of the transformer, especially in Part 2 of the series.

## Deeper Understanding
These articles provide an in-depth view of attention mechanisms -

1. [Understanding and coding attention, Sebastian Raschka](https://substack.com/inbox/post/140464659)
2. [Brandon Rohrer’s Transformers from scratch](https://e2eml.school/transformers.html)
3. [A mathematical framework for transformer circuits](https://transformer-circuits.pub/2021/framework/index.html)
4. [Creating a Transformer From Scratch](https://benjaminwarner.dev/2023/07/01/attention-mechanism)
5. [How to scale your model](https://jax-ml.github.io/scaling-book/) 
6. [Transformers Laid Out](https://goyalpramod.github.io/blogs/Transformers_laid_out/)
7. [Everything about Transformers](https://www.krupadave.com/articles/everything-about-transformers?x=v3)

# Convolutional Neural Networks
1. Go through Brandon Rohrer’s [How do CNNs work? Video and Notes](https://e2eml.school/how_convolutional_neural_networks_work) and the [in-depth video](https://www.youtube.com/watch?v=JB8T_zN7ZC0) to conceptually understand
	- Convolutional Layers
	- Pooling Layers
	- Normalization Layers (ReLU, Sigmoid)
2. Read Chapter ?? From Deep Learning book by Christopher Bishop

## UNets 

UNets are fundamental to diffusion models, and therefore gaining a good understanding of how they work is critical. 

1. [The U-Net (actually) explained in 10 minutes](https://www.youtube.com/watch?v=NhdzGfB1q74)
2. Read paper U-Net: Convolutional Networks for Biomedical Image Segmentation

### Attention in UNets
- [How is attention added to the UNet blocks?](https://huggingface.co/blog/perceiver): This article explains the Perceiver model that allows interleaving of attention blocks with the CNN blocks.
- Read the following papers - 
	- [Perceiver](https://arxiv.org/abs/2103.03206) and [PerceiverIO](https://arxiv.org/abs/2107.14795)
	- [Non-Local Neural Networks](https://arxiv.org/abs/1711.07971)
- There is a code implementation explanation for UNets with Attention layers here - https://nn.labml.ai/diffusion/stable_diffusion/model/unet_attention.html 

# Diffusion Models
## Conceptual Understanding 

1. [How AI Image Generators Work](https://www.youtube.com/watch?v=1CIpzeNxIhU) : Excellent introduction to the fundamental workings of UNet in the context of Stable Diffusion from [`computerphile`](https://www.youtube.com/@Computerphile).
2. [Stable Diffusion in Code](https://www.youtube.com/watch?v=-lz30by8-sU) : Introduction to basic code structure and components of Stable Diffusion from [`computerphile`](https://www.youtube.com/@Computerphile). Head over to [Google Colab](https://colab.research.google.com/drive/1roZqqhsdpCXZr8kgV_Bx_ABVBPgea3lX?usp=sharing) for code. This provides a first level down (from using `pipelines` in `diffuser` library) of running UNets iteratively. Also provides examples of how to blend between multiple prompts. 
2. [How Stable Diffusion Works](https://www.youtube.com/watch?v=sFztPP9qPRc): This video is slightly advanced, but it shows how attention mechanisms are combined with UNets in latent space for stable diffusion

1. *Diffusion Model Clearly Explained!* [Part 1](https://medium.com/@steinsfu/diffusion-model-clearly-explained-cd331bd41166) and [Part 2](https://medium.com/@steinsfu/stable-diffusion-clearly-explained-ed008044e07e) are good introductory articles to provide an overview of how diffusion models work.

3. **[LoRA — Intuitively and Exhaustively Explained](https://medium.com/towards-data-science/lora-intuitively-and-exhaustively-explained-e944a6bff46b)** This article provides a good intuitive explanation of what LoRA is and how it works. Note that LoRA is part of a family of fine-tuning approaches called “PEFT” - **Parameter Efficient Fine-Tuning**. This approach is **key to understanding how one can efficiently and quickly fine-tune a foundational diffusion model with new data**.
	- [Here is a video explainer from the LoRA authors at Microsoft](https://www.youtube.com/watch?v=DhRoTONcyZE) 
	- HuggingFace has a [PEFT library](https://github.com/huggingface/peft) to use with [diffusers](https://github.com/huggingface/diffusers).	 
4. **[Classifer-free Guidance](https://sander.ai/2022/05/26/guidance.html)**: Once a reasonable understanding of inner workings of stable diffusion is gained from [`computerphile's`](https://www.youtube.com/@Computerphile) videos above, this article provides a mathematical intuition on how classifier-free guidance works. **Classifier-free guidance is key for how conditioning works in stable diffusion**.
5. [**ControlNets** clearly explained!](https://medium.com/@steinsfu/stable-diffusion-controlnet-clearly-explained-f86092b62c89) is a good article providing an overview of how ControlNets are used for more advanced guidance with diffusion models.


## Hands-on Tutorials

5.  [CVPR Tutorial on Denoising Diffusion Models](https://cvpr2022-tutorial-diffusion-models.github.io)
1. [Stable Diffusion in Code](https://colab.research.google.com/drive/1roZqqhsdpCXZr8kgV_Bx_ABVBPgea3lX?usp=sharing): This provides a first level down (from using `pipelines` in `diffuser` library) of running UNets iteratively. Also provides examples of how to blend between multiple prompts. This is a companion code to the video [Stable Diffusion in Code](https://www.youtube.com/watch?v=-lz30by8-sU) above.
2. [Understanding Stable Diffusion from “Scratch”](https://scholar.harvard.edu/binxuw/classes/machine-learning-scratch/materials/stable-diffusion-scratch) is a bit outdated, but still a good step-by-step tutorial (co-lab notebook) to walk-through for Stable Diffusion.
3. [Introductory tutorial for Huggingface Diffuser library](https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/diffusers_intro.ipynb)  
4.  [The annotated diffusion model](https://huggingface.co/blog/annotated-diffusion) by Huggingface


The following links have not been reviewed -
1. https://course.fast.ai/Lessons/lesson9.html
2. https://www.youtube.com/watch?v=_7rMfsA24Ls&t=5s
3. https://www.youtube.com/watch?v=ZBKpAp_6TGI 

# Vision Transformers
- Sebastian Raschka
	- [State of Computer Vision 2023](https://magazine.sebastianraschka.com/p/ahead-of-ai-10-state-of-computer?utm_source=%2Finbox%2Fsaved&utm_medium=reader2)
	- [Understanding Large Language Models](https://magazine.sebastianraschka.com/p/understanding-large-language-models)
- Sayak Paul’s [CVPR 2023 Tutorial](https://all-things-vits.github.io/atv/) on Vision Transformers
- https://medium.com/towards-data-science/vision-transformers-explained-a9d07147e4c8
- https://mhamilton.net/featup.html

# Evolution of Generative Architectures for Image Synthesis
- [Google Imagen](https://imagen.research.google) [May 2022]
- [Google Parti](https://sites.research.google/parti/) [June 2022]
- [Google Muse](https://muse-model.github.io) [Jan 2023]
	- [Blog explaining Muse](https://blog.metaphysic.ai/muse-googles-super-fast-text-to-image-model-abandons-latent-diffusion-for-transformers/)

# Transformers vs CNNs 
- [On the speed of ViTs and CNNs](http://lucasb.eyer.be/articles/vit_cnn_speed.html)

# Other Blogs
- http://colah.github.io
- https://distill.pub/2020/circuits/
- https://transformer-circuits.pub
- [Sebastian Raschka’s Blog](https://magazine.sebastianraschka.com)
- [Pramod Goyal Blog](https://goyalpramod.github.io/blog/)