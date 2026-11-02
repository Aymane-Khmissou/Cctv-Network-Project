# Network Architecture

```mermaid
flowchart TD
  NET((Internet)) --> RTR[Huawei Router<br/>DHCP / Wi-Fi]
  RTR --> SW[TP-Link Switch]
  SW --> XVR[Dahua XVR + HDD]
  SW --> PC1[PC 1 - Admin]
  SW --> PC2[PC 2 - Accountant]
  SW --> PRN[Printer]
  SW --> TKT[Ticketing system]
  XVR --> CAM[6 cameras]
  XVR --> MON[Large monitor]
  XVR --> TV[TV]
  XVR -. P2P .-> MOB[Owner's mobile app]
```

## Design decisions
- **Flat network with DHCP**: only the admin and the accountant use the PCs, so VLAN segmentation was not required.
- **Cameras on the XVR**: the recorder centralizes recording and local display.
- **Remote access via P2P** to avoid opening ports on the router.
- **Printer and ticketing system** connected directly to the system so printing no longer depends on fragile PC settings. [adapt to your real setup]
