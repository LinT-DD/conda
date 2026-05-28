# Split Archive

This directory contains split parts for `megatron-b200-full-conda-env.tar.gz`.

Reassemble:

```bash
cat megatron-b200-full-conda-env.tar.gz.part-* > megatron-b200-full-conda-env.tar.gz
sha256sum -c megatron-b200-full-conda-env.tar.gz.sha256
```
