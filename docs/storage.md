# Storage Architecture

## Storage Philosophy
- Speed where needed
- Redundancy where critical
- Simplicity over unnecessary complexity

## Storage Layout Diagram

```mermaid
flowchart LR
    Cache[NVMe Cache\nZFS]
    Mirror[Studymirror Pool\nZFS Mirror]
    Bigpool[Bigpool\nZFS Single Disk]
    Array[XFS Array Disk]

    Cache --> Mirror
    Cache --> DockerData[Appdata & Databases]
    Mirror --> Photos[Immich Originals]
    Mirror --> Docs[Documents & Backups]
    Bigpool --> Cold[Cold Storage]
