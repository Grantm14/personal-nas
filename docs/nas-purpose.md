# NAS Purpose and Usage

## Project Purpose

This NAS is my primary self-hosted infrastructure platform.
It supports real personal workflows while serving as a hands-on learning
environment for systems engineering, networking, and storage design.

The system is intentionally modular and documented as it evolves, reflecting
the way production infrastructure is designed and maintained.
> For planned enhancements, see the [NAS Roadmap](nas-roadmap.md).<br/>
> Back to [Repository Overview](../README.md).


## Core Design Goals

- Maintain long-term ownership of personal data
- Replace or reduce reliance on third-party cloud services
- Provide fast local access from a wired workstation
- Use production-style tooling in a realistic environment
- Design with future expansion in mind

## How I Use This NAS

### Photo and Media Management (Immich)

Immich functions as a self-hosted replacement for Google Photos.
It stores and indexes all personal photos and videos while preserving
original quality and metadata.

Configuration highlights:
- Databases and cache reside on NVMe storage
- Original media files live on mirrored HDDs
- Optimized for fast local access and long-term retention

### Document and File Management

This system centralizes personal documents, notes, and project files.
The goal is consistent access across devices without dependence on
cloud subscriptions.

### General Storage and Workflows

The NAS also supports:
- Lightroom photo libraries
- Project archives
- Backup copies of important data

Local storage avoids bandwidth limitations and recurring storage costs.

## Architectural Summary

- Unraid OS manages hardware, disks, and shares
- Docker isolates applications and dependencies
- ZFS provides redundancy where data integrity matters
- NVMe is reserved for active workloads and databases
- HDDs are used for capacity and durability
