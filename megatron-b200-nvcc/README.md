# Split Archive

This directory contains split parts for `megatron-b200-nvcc-conda-env.tar.gz`.

Reassemble:

```bash
cat megatron-b200-nvcc-conda-env.tar.gz.part-* > megatron-b200-nvcc-conda-env.tar.gz
test "$(sha256sum megatron-b200-nvcc-conda-env.tar.gz | cut -d ' ' -f1)" = "$(cut -d ' ' -f1 megatron-b200-nvcc-conda-env.tar.gz.sha256)" && echo OK
```

This package includes CUDA 12.8 `nvcc`, CUDA headers/libs, `regex==2026.5.9`, `six`, Apex fused wgrad, and Transformer Engine.
