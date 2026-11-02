# Router and Switch Configuration (sanitized)

## Huawei router
- DHCP enabled with a defined range
- Reserved addresses for XVR, printer, ticketing system [confirm]
- Admin password changed [confirm]
- Wi-Fi: WPA2/WPA3 with strong key [confirm]
- Remote management disabled [confirm]
- No port forwarding: remote access via P2P

## TP-Link switch
- Unmanaged/managed: [specify]
- Port allocation: XVR, PC 1, PC 2, printer, ticketing system, uplink to router
- Cables tested and labeled

## Segmentation
No VLANs. Justification: small network, only the admin and the accountant use the PCs.
Possible future improvement: separate camera/XVR traffic in a dedicated VLAN.
