
---

## 📄 `docs/hardware.md`
```markdown
# Hardware Overview

## Base System
- Platform: Dell OptiPlex 7050
- CPU: Intel i5-6600 (4 cores)
- RAM: 40 GB DDR4
- Network: Intel I219-LM (1 Gbps)

## Storage Hardware
- Boot Device: 64 GB USB
- NVMe Cache: 256 GB NVMe SSD
- Mirrored HDD Pool: 2 × 1 TB HDDs
- Additional Pool: 2 TB HDD
- Array Disk: 500 GB HDD

## Design Rationale
This hardware was selected to balance:
- Cost efficiency
- Low power consumption
- Sufficient performance for Docker workloads
- Learning value over raw performance

## Known Limitations
- Gigabit networking bottleneck
- Limited internal drive expansion
- No dedicated GPU (planned upgrade)
