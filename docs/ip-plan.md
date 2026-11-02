# IP Addressing Plan

> Example values only. Do not publish real public IPs or credentials.

- **Network:** 192.168.1.0/24 (example)
- **Gateway:** 192.168.1.1 (Huawei router)
- **DHCP range:** 192.168.1.100 - 192.168.1.200 (example)
- **VLANs:** none (see architecture decisions)

| Device | Role | IP assignment | Example IP |
|---|---|---|---|
| Huawei router | Gateway / DHCP | Static | 192.168.1.1 |
| TP-Link switch | Switching | [DHCP/Static] | [192.168.1.2] |
| Dahua XVR | Recorder | [DHCP reservation recommended] | [192.168.1.10] |
| PC 1 | Admin | DHCP | dynamic |
| PC 2 | Accountant | DHCP | dynamic |
| Printer | Printing | [DHCP reservation recommended] | [192.168.1.20] |
| Ticketing system | Tickets | [DHCP/Static] | [192.168.1.21] |

**Recommendation:** reserve IPs (DHCP binding by MAC) for XVR, printer and ticketing system so addresses never change.
