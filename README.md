# megatron-b200-full

Offline Conda environment package for B200 Megatron work.

Contents:

```text
Python 3.12.13
PyTorch 2.12.0.dev20260408+cu128
CUDA toolkit 12.8 packages
Apex with fused_weight_gradient_mlp_cuda built for sm_100
Transformer Engine 2.15.0
```

## Reassemble

```bash
cd megatron-b200-full
cat megatron-b200-full-conda-env.tar.gz.part-* > megatron-b200-full-conda-env.tar.gz
sha256sum -c megatron-b200-full-conda-env.tar.gz.sha256
```

## Install On B200

```bash
mkdir -p /opt/conda/envs/megatron-b200
tar -xzf megatron-b200-full-conda-env.tar.gz -C /opt/conda/envs/megatron-b200
/opt/conda/envs/megatron-b200/bin/conda-unpack
conda activate /opt/conda/envs/megatron-b200
```
