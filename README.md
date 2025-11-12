# MLOS Linux Kernel Patches

**Shared Kernel Patches for MLOS Linux Distributions**

This repository contains MLOS-specific kernel patches that implement kernel-level optimizations for machine learning workloads as specified in patent US-63/865,176.

[![License: Proprietary](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)
[![Status: Planning](https://img.shields.io/badge/Status-Planning-orange)](https://github.com/mlOS-foundation/mlos-linux-kernel)
[![Patent: US-63/865,176](https://img.shields.io/badge/Patent-US--63%2F865%2C176-blue)](https://github.com/mlOS-foundation/patent-docs)

## Overview

This repository provides kernel patches for both Ubuntu and Flatcar-based MLOS Linux distributions. The patches implement:

1. **ML-Aware Kernel Scheduler** - Priority-based ML task scheduling with tensor operation awareness
2. **Tensor Memory Management** - Zero-copy tensor operations and shared memory
3. **GPU Resource Orchestration** - Multi-model GPU coordination and hardware abstraction

## IP Protection

**Note:** This repository is **public** but contains only:
- ✅ Patch files (applied, not source code)
- ✅ Kernel configuration files
- ✅ Documentation

**Private Components:**
- 🔒 Source code for kernel modifications (in private repository)
- 🔒 Development history and internal documentation

Patches are published as **signed binary artifacts** from the private repository. This public repository serves as a reference and distribution point for verified patches.

## Patch Structure

```
patches/
├── mlos-scheduler.patch        # ML-aware scheduler implementation
├── tensor-memory.patch         # Tensor memory management
└── gpu-orchestration.patch     # GPU resource orchestration

config/
├── ubuntu/                     # Ubuntu kernel configuration
│   └── config-6.1.x
└── flatcar/                    # Flatcar kernel configuration
    └── config-6.1.x
```

## Usage

### For Distribution Builds

Patches are downloaded and verified during distribution builds:

```bash
# Patches are downloaded from private registry
# Verified with GPG signatures
# Applied during kernel build process
```

### For Kernel Developers

```bash
# Apply patches to base kernel
cd linux-6.1.x
for patch in patches/*.patch; do
    patch -p1 < $patch
done

# Configure kernel
cp config/ubuntu/config-6.1.x .config
make oldconfig
make
```

## Standards Compliance

- ✅ **Linux Kernel API Compliance** - Follows kernel coding standards
- ✅ **Scheduler API** - Standard scheduler interface
- ✅ **POSIX Shared Memory** - Standard shared memory API
- ✅ **DRM/KMS API** - Standard GPU interface

## Patent Information

These patches implement innovations from:
- **US-63/865,176**: Kernel-Level Optimizations for Machine Learning Workloads

See [patent-docs](https://github.com/mlOS-foundation/patent-docs) for complete patent information.

## Related Repositories

- [mlos-linux-ubuntu](https://github.com/mlOS-foundation/mlos-linux-ubuntu) - Ubuntu-based distribution
- [mlos-linux-flatcar](https://github.com/mlOS-foundation/mlos-linux-flatcar) - Flatcar-based distribution
- [core](https://github.com/mlOS-foundation/core) - MLOS Core runtime (private)

## Status

**Current Status:** Planning Phase  
**Target Release:** v1.0.0 - Q2-Q3 2026

## License

**Proprietary License** - See [LICENSE](LICENSE) for details.

These patches are patent-pending and proprietary to MLOS Foundation.

---

**MLOS Foundation** - Building the future of ML infrastructure.

