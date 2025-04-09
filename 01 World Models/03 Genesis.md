# 03 Genesis

https://genesis-embodied-ai.github.io

- Taichi is not supported (yet) on [rocm](https://github.com/taichi-dev/taichi/issues/6434).


	TAICHI_CMAKE_ARGS="-DTI_WITH_VULKAN=ON -DTI_WITH_OPENGL=ON -DTI_BUILD_TESTS=ON -DTI_BUILD_EXAMPLES=OFF  -DCMAKE_CXX_COMPILER=/opt/rocm/llvm/bin/clang++ -DTI_WITH_AMDGPU=ON" python setup.py develop