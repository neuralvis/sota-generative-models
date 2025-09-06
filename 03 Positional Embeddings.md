# 03 Positional Embeddings

- [understanding ROPE Embedding](https://blog.ngxson.com/very-simple-to-understand-rope-2drope-mrope)


## Representations

- V-JEPA 2 ? What does it do ? 
- The tension between encoding semantics vs. encoding spatial understanding
	- The Janus-Pro paper articulates this clearly. 
- Fuxin’s work
	- https://mingqij.github.io/projects/gs4/
	- https://github.com/apple/ml-autofocusformer


There seems to be two disconnected paradigms for “visual encodings”

1. High level semantic encoding (for text alignment, captioning etc.) - by SIGLIP and CLIP - like Models. Requires high level semantic understanding and reasoning. Encoding task focuses on high-dimensional representations to capture this. 
2. Providing low-level encoding (for perception and generation tasks): The family of VAEs (VQ-VAE, etc) and the likes of DINOv3 fall into this category. 

The original Janus paper - https://arxiv.org/abs/2410.13848 articulates and discusses this conceptually. 

Where does VJEPA 2 (by meta) fall in this mental model ?
Janus says we cannot unify these representations. Why ? What are the fundamental issues with doing this ? 

Do these papers attempt to address this issue ?

- [C. Ziwen et al. AutoFocusFormer: Image Segmentation off the Grid. CVPR 2023.](https://github.com/apple/ml-autofocusformer)
- [GS4: Generalizable Sparse Splatting Semantic SLAM](https://mingqij.github.io/projects/gs4/). ? 