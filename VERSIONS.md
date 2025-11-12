# MLOS Kernel Patches Version Compatibility

## Current Target: v1.0.0

**Patches:**
- **ML-Aware Scheduler:** v1.0.0
- **Tensor Memory Management:** v1.0.0
- **GPU Resource Orchestration:** v1.0.0

**Kernel Compatibility:**
- **Base Kernel:** Linux 6.1+ (LTS recommended)
- **Ubuntu:** Ubuntu kernel 6.1+
- **Flatcar:** Flatcar kernel 6.1+

## Version Matrix

| Kernel Patches | Base Kernel | Ubuntu Support | Flatcar Support | Status |
|----------------|-------------|---------------|-----------------|--------|
| v1.0.0 (target)| 6.1+        | ✅            | ✅              | 🔄 Planning |

## Patch Details

### ML-Aware Scheduler (v1.0.0)
- Scheduler class: `SCHED_ML`
- Priority-based ML task scheduling
- Tensor operation awareness
- Model context switching

### Tensor Memory Management (v1.0.0)
- Zero-copy tensor operations
- Shared memory mechanisms
- GPU memory orchestration

### GPU Resource Orchestration (v1.0.0)
- Hardware abstraction layer
- Unified GPU interface
- Multi-model coordination

## Distribution Usage

**Ubuntu:**
- Patches applied during kernel build
- Configuration: `config/ubuntu/config-6.1.x`

**Flatcar:**
- Patches applied during kernel build
- Configuration: `config/flatcar/config-6.1.x`

---

**Note:** Patches are published as signed artifacts from private repository. See [IP Protection Plan](https://github.com/mlOS-foundation/core/blob/main/docs/DISTRO_IP_PROTECTION_PLAN.md) for details.

