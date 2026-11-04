# CCTV \& Local Network Deployment: Real-World Project

> Redesign and deployment of a video surveillance system and a small-office network (cameras, PCs, phone, printer, ticketing system) for a client whose previous installation was unreliable.

**Type:** Real client project \| **Year:** 2026 \| **Role:** Installation, network configuration, troubleshooting, documentation **Client:** \[Retail shop / office / business type, name omitted for confidentiality\]

---

## 1. Context and Client Need

The client's main concern was **security**. The existing setup had been poorly installed:

- Cameras were working badly or not at all
- **No hard drive** in the recorder, so **no recording or storage**
- The **ticket-issuing system and the printer** did not work reliably with the PCs (sometimes working, sometimes not)
- Configuration was missing or inconsistent

## 2. Objectives

1. Reliable **live monitoring** on-site and **recording** with proper storage
2. **Remote viewing** from a mobile phone
3. Stable communication between **PCs, printer, ticketing system and network**
4. Clean **cable management** and a clear, documented layout
5. Good-quality equipment at a **reasonable price**

## 3. Hardware

| Equipment | Details |
| --- | --- |
| Recorder | Dahua XVR (4.0) |
| Cameras | 6 cameras
| Storage | Hard drive: 2 TB |
| Router | Huawei |
| Switch | TP-Link  |
| Display | 1 large monitor + 1 TV (live view) |
| Computers | 2 PCs |
| Phone | 1 mobile phone (remote viewing) |
| Printer | Connected directly to the system/PC |
| Ticketing system | HP, integrated with the printer |

## 4. Network Architecture

```
            Internet
               |
         [Huawei Router]  (DHCP)
               |
         [TP-Link Switch]
   ┌─────┬──────┼───────┬──────────┐
 [XVR]  [PC 1] [PC 2] [Printer] [Ticket system]
   |
 6 cameras  ──► Monitor + TV (local display)
   |
 Remote access via P2P ──► Mobile phone
```

> Add your own diagram in `diagrams/` (draw.io or Packet Tracer) and link it here: `![Network diagram](diagrams/network-diagram.svg)`

**Addressing:** DHCP on the Huawei router \[with static reservations for XVR/printer: yes/no\]. **VLANs:** Not deployed. Only the admin and the accountant have access to the PCs, so segmentation was not required for this environment.

## 5. Work Performed

### Installation

- Installed and aligned **6 cameras** in locations chosen for coverage of key areas
- Structured cabling (RJ45 / power), with clean routing and labeling
- Installed the **hard drive** in the XVR and initialized it

### Configuration

- **XVR:** recording mode and schedule, **overwrite policy** when disk is full, local display on monitor and TV
- **Remote access:** **P2P** setup and mobile app configuration on the owner's phone
- **Router/switch:** network integration of all devices
- **Printer and ticketing system:** direct connection and stable communication with the PCs

### Equipment selection

- Replaced faulty components and selected **the best quality/price ratio** equipment for the client's budget

## 6. Problems Encountered and Solutions

| Problem | Cause | Solution |
| --- | --- | --- |
| Cameras unreliable | Poor initial installation | Re-installed and re-tested each camera |
| No recording | No hard drive in the XVR | Installed disk, configured recording and overwrite |
| Ticket system and printer working intermittently | Missing/inconsistent configuration | Reconfigured connection between PCs, printer and ticket system |
| Early hardware issue | \[Describe: faulty device, cable, etc.\] | \[Replacement / fix\] |
| Cable and power disorder | No planning | Planned layout and organized cabling |

## 7. Results

- ✅ All 6 cameras working, **live view** on large monitor and TV
- ✅ **Continuous recording** to hard drive, with automatic overwrite
- ✅ Stable **remote access** from mobile
- ✅ Printer and ticketing system **working reliably** with PCs
- ✅ Organized cabling and a stable network
- ✅ **Very satisfied client**, who was particularly pleased with the stability after the previous experience

## 8. Skills Demonstrated

`CCTV / IP surveillance` · `Dahua XVR` · `TCP/IP` · `DHCP` · `LAN setup` · `Router & switch configuration` · `P2P remote access` · `Troubleshooting` · `Structured cabling` · `Technical documentation`

## 9. Security Notes

- Default passwords changed on XVR and router: \[confirm\]
- Firmware updated: \[confirm\]
- Access restricted to authorized users (admin + accountant)
- Sensitive data (passwords, public IPs, serial numbers) is **not** included in this repository

## 10. Repository Structure

```
cctv-network-project/
├── README.md
├── docs/
│   ├── network-architecture.md   # diagram (Mermaid) + explanation
│   ├── equipment-list.md         # bill of materials
│   ├── ip-plan.md                # addressing plan (example values)
│   ├── installation-log.md       # step-by-step work log
│   ├── xvr-configuration.md      # recorder settings
│   ├── router-switch-config.md   # router/switch settings
│   ├── troubleshooting.md        # problems and fixes
│   ├── test-checklist.md         # acceptance tests
│   └── handover-maintenance.md   # client handover + maintenance
├── diagrams/network-diagram.svg

```

## 11. Author

**\[KHMISSOU Aymane\]**: \[www.linkedin.com/in/aymane-khmissou\] · \[aymanekhmissou@gmail.com\]
