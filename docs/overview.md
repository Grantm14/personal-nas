# NAS System Overview

This project documents my personal self-hosted NAS built on Unraid.
It is designed for long-term storage, photo archival, productivity tools,
and hands-on learning with real infrastructure.

## High-Level Architecture

```mermaid
flowchart TD
    PC[Desktop PC]
    Phone[Phone]
    Laptop[Laptop]

    VPN[WireGuard VPN]

    NAS[Unraid NAS]
    Docker[Docker Services]
    Storage[Storage Pools]

    PC --> VPN
    Phone --> VPN
    Laptop --> VPN

    VPN --> NAS
    NAS --> Docker
    NAS --> Storage
