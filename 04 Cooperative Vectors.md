# 04 Cooperative Vectors


- Introductory Link from PCGamer: https://www.pcgamer.com/hardware/graphics-cards/amd-intel-microsoft-and-nvidia-are-all-excited-about-cooperative-vectors-and-what-they-mean-for-the-future-of-3d-graphics-but-its-going-to-be-a-good-while-before-we-really-see-their-impact/
 
```
Cooperative vectors is the name for an additional API to the DirectX 12 family, that will allow programmers to directly use a GPU's matrix or tensor cores, without having to use the vendor's specific API. For example, in the case of Nvidia's GeForce RTX cards, the Tensor cores automatically handle any FP16 calculations but otherwise, you need to use the likes of CUDA to program them. The DX12 CoopVec API gets around this issue, as it will be supported by AMD, Intel, Nvidia, and even Qualcomm.
 
You could argue that CoopVec is really just a bunch of extra HLSL (High Level Shader Language) instructions that are specific to matrix-vector operations, which tensor/matrix cores are designed to accelerate. But a better way to look at the API is that it is all about bringing the world of 'little AI' into shaders.
```
 
### Cooperative Vectors
 
```
AMD didn't have much to say either. Its speaker, Joe Rozek, went through something entirely different: the neural lighting system used for its recent Toy Shop demo, yes, the one which left our Andy a bit underwhelmed. Rozek somewhat quietly pointed out that CoopVec is currently only supported on its latest RNDA 4-power Radeon RX 9070 graphics cards, though AMD is looking to see if older Radeons can support it too.
```
 
**Not a lot of information here:**
- https://devblogs.microsoft.com/directx/enabling-neural-rendering-in-directx-cooperative-vector-support-coming-soon/
- Specs: https://github.com/microsoft/hlsl-specs/blob/main/proposals/0029-cooperative-vector.md
 
**Detailed Presentation**
- Vulcanized 2025: Machine Learning in Vulkan with Cooperative Matrix 2
                - [Slides](https://www.vulkan.org/user/pages/09.events/vulkanised-2025/T47-Jeff-Bolz-NVIDIA.pdf)
                - [Video Recording](https://youtu.be/gG-rxpeLGA8)
- Vulcanized 2025: Using MLPs in Shaders
                - [Slides](https://www.vulkan.org/user/pages/09.events/vulkanised-2025/T48-Jeff-Bolz-NVIDIA.pdf)
                - [Video Recording](https://youtu.be/fF2HfxkpSog)
 
 
### Tools
- https://shader-slang.org
- https://github.com/shader-slang/slangpy?tab=readme-ov-file
- [Differences between Shaders and Tensor Languages](https://developer.nvidia.com/blog/differentiable-slang-a-shading-language-for-renderers-that-learn/)
 
 
**WMMA**
 
- RDNA 3 WMMA: https://gpuopen.com/learn/wmma_on_rdna3/
- RDNA 4 WMMA:
    - https://chipsandcheese.com/p/examining-amds-rdna-4-changes-in-llvm
- RDNA 4 Architecture Overview
	- RDNA 4 Architecture Overview: https://chipsandcheese.com/p/amds-rdna4-architecture-video
  - RDNA 4 Specs Toms HW: https://www.tomshardware.com/pc-components/gpus/amd-rdna4-rx-9000-series-gpus-specifications-pricing-release-date#section-rdna-4-gpu-specifications
  - WCCTech : https://wccftech.com/amd-rdna-4-architecture-deep-dive-new-compute-units-raytracing-cores-ai-enhancements-path-tracing/#:~:text=The%20core%20building%20block%20of,Structured%20Sparsity%20for%20%2B2x%20rate