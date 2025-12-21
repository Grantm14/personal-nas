
---

## 📄 `docs/services.md`
```markdown
# Services & Applications

## Core Services

### Immich
- Purpose: Self-hosted photo and video library
- Storage:
  - Originals: ZFS mirror
  - Database & cache: NVMe

### Document Sync (Planned)
- Sync notes and PDFs across devices
- Auto-sorting by type and date

### Finance Management (Planned)
- Self-hosted budgeting and expense tracking
- Privacy-focused data storage

### iSCSI Share
- Network block storage for Lightroom catalogs
- High reliability and consistent latency

## Service Relationships

```mermaid
flowchart TD
    Immich --> Postgres
    Immich --> Redis
    Immich --> PhotoStore[Photo Storage]

    Postgres --> Cache
    Redis --> Cache
    PhotoStore --> Mirror
