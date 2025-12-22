# Network Architecture Overview

This diagram documents the physical and logical network layout of my home NAS
environment. The design prioritizes simplicity, correct role separation, and
clear traffic flow.

## High-Level Network Topology

```mermaid
flowchart TD
    Internet[Internet<br/>Fiber Connection]

    Calix[Calix ISP Router<br/>Gateway: NAT, DHCP, Firewall<br/>~1 Gbps Up / Down]

    Wireless[Wireless Devices<br/>Phones, IoT, Guests]

    RoomRouter[Room Router<br/>Access Point Mode<br/>No NAT<br/>No DHCP<br/>Local switching only<br/>100 Mb/s uplink]

    NAS[NAS Server<br/>Ethernet<br/>Unraid OS]

    %% Network flow
    Internet --> Calix
    Calix --> RoomRouter
    RoomRouter --> NAS

    %% Side branch
    Calix --> Wireless
