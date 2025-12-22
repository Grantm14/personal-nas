# Personal NAS & Self-Hosted Infrastructure

This repository documents the design, architecture, and ongoing evolution of
my personal NAS and self-hosted infrastructure platform. The system is built
around Unraid and Docker, and is designed to support real personal workflows
such as photo management, document organization, and long-term data storage.

Rather than a single-purpose server, this NAS is treated as a modular,
well-documented system that evolves alongside my technical skills.

---

## What This System Does

- Centralizes long-term personal data under my control
- Replaces or reduces reliance on third-party cloud services
- Provides fast local access from a wired workstation
- Uses production-style tooling in a realistic environment
- Serves as a hands-on learning platform for systems engineering

---

## System Documentation Map

Start here and explore deeper as needed:

### Network & Infrastructure
- [Network Overview](docs/overview-network.md)

### NAS Architecture
- [NAS Internal Structure](docs/nas-structure.md)
- [NAS Purpose and Usage](docs/nas-purpose.md)
- [NAS Roadmap and Future Plans](docs/nas-roadmap.md)

Additional deep-dive documentation is added as the system evolves.

---

## Technologies Used

- **Unraid OS** – host operating system and storage management
- **Docker** – application isolation and service management
- **ZFS** – data integrity and redundancy
- **NVMe SSDs** – cache and active workloads
- **HDD storage** – long-term, high-capacity data storage
- **Wire-speed Ethernet** – local access from primary workstation

---

## Project Status

This is an actively maintained system.  
Changes are intentional, documented, and driven by real usage rather than
hypothetical requirements.

Planned enhancements and experiments are tracked in the
[NAS Roadmap](docs/nas-roadmap.md).

---

## Why This Project Exists

This repository is both:
- A practical record of a real system I rely on daily
- A portfolio piece demonstrating systems thinking, documentation, and design

The emphasis is on clarity, correctness, and long-term maintainability rather
than one-off setup instructions.
