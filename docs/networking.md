
---

## 📄 `docs/networking.md`
```mermaid
# Networking & Access

## Network Model

```mermaid
flowchart TD
    Internet --> VPN[WireGuard VPN]
    VPN --> NAS[Unraid NAS]
    NAS --> Services[Docker Services]
