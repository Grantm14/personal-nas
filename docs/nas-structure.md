# NAS Internal Architecture
This diagram shows the internal structure of the NAS server, focusing on how
compute, applications, and storage are layered on top of the physical hardware.
- [Purpose and Usage](nas-purpose.md)
- [Roadmap and Future Plans](nas-roadmap.md)
- [Repository Overview](../README.md)


## NAS Structure Overview

```mermaid
flowchart TD
    NAS[
    <b>NAS Server</b><br/>
    192.168.1.198
    Unraid OS
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
    NVMe SSD: used for cache<br/>
    Mirrored 1tb HDDs: used for main data<br/>
    2tb single HDD: For Lightroom Pics
    ]

    NAS --> Docker
    NAS -->Storage
    Docker --> Apps
    Storage --> Disks
```

## Notes

- Unraid provides the host OS and manages disk aggregation and sharing.
- Docker is used to isolate applications and services.
- Applications store persistent data on managed storage pools.
- Physical disks are abstracted away from applications through Unraid.
```
