# NAS Internal Architecture

This diagram shows the internal structure of the NAS server, focusing on how
compute, applications, and storage are layered on top of the physical hardware.

## NAS Structure Overview

```mermaid
flowchart TD
    NAS[
    <b>NAS Server</b><br/>
    Dell OptiPlex<br/>
    Ethernet
    ]

    OS[
    <b>Unraid OS</b><br/>
    Host Operating System
    ]

    Docker[
    <b>Docker Engine</b><br/>
    Container Runtime
    ]

    Apps[
    <b>Applications</b><br/>
    Immich<br/>
    Document Management<br/>
    Other Services
    ]

    Storage[
    <b>Storage Layer</b><br/>
    ZFS Pools<br/>
    XFS Array
    ]

    Disks[
    <b>Physical Disks</b><br/>
    NVMe SSD<br/>
    HDDs
    ]

    NAS --> OS
    OS --> Docker
    Docker --> Apps
    OS --> Storage
    Storage --> Disks
```

## Notes

- Unraid provides the host OS and manages disk aggregation and sharing.
- Docker is used to isolate applications and services.
- Applications store persistent data on managed storage pools.
- Physical disks are abstracted away from applications through Unraid.
```
