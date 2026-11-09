# `oodrv-accel`

Ring-3 Compute Accelerator driver suite: GPU compute command queue & doorbell rings (CUDA / ROCm / Vulkan-Compute usermode submission), NPU/TPU systolic matrix engines (`INT4`/`INT8`/`FP8`/`BF16`), CXL 3.0 Type-2/Type-3 coherent memory & peer-DMA fabric, and hardware crypto / post-quantum (`ML-KEM-768`, `ML-DSA-65`, `SHA-3`, `Keccak`) + compression QAT offload for [openOODA](https://openOODA.org) (`L1` • [`@openOODA-kernel`](https://github.com/openOODA-kernel)).

- **Personas / Subcommands**: `oodrv-accel`, `oodrv-gpu`, `status`, `verify`, `inspect [path]`, `load <path>`, `about`
- **Capabilities (`CapReg64`)**: `FsReadCap`, `FsWriteCap`, `DmaCap`, `MmioCap`, `GpuCap`, `PciCap`
- **Bundle**: `@kernel` (`oopm install @kernel` or `oopm install oodrv-accel`)

## Usage

```sh
oodrv-accel status            # Inspect GPU cmd queues, NPU tiles, CXL HDM windows & QAT rings
oodrv-accel verify            # Verify VRAM BAR bounds, tile descriptors, HDM coherence & key-slot isolation
oodrv-accel inspect [path]    # Inspect accelerator transport & offload configuration
oodrv-accel about
```

## Build & Test

```sh
make build
make test
```
