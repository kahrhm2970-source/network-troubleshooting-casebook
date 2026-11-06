# Verification matrix
All actual results remain pending. A failed ping alone does not prove an ACL or root cause.

| Check | Command or action | Expected outcome | Actual |
|---|---|---|---|
| VLAN mapping | SW1 show vlan brief | Fa0/1..4 mapped to VLAN 10,20,30,99 | Pending |
| Trunk | SW1 show interfaces trunk | G0/1 trunking, VLANs 10,20,30,99,999 allowed, native 999 | Pending |
| Routing | R1 show ip interface brief | Parent G0/0 and subinterfaces up/up | Pending |
| Staff DHCP | Staff ipconfig, R1 show ip dhcp binding | 10.10.10.11–254, /24, gateway .1 | Pending |
| Guest DHCP | Guest ipconfig | 10.10.20.11–254, /24, gateway .1 | Pending |
| Staff to camera | Staff ping 10.10.30.10 | Success after ARP | Pending |
| Admin to camera | Admin ping 10.10.30.10 | Success after ARP | Pending |
| Admin to switch | Admin ping 10.10.99.2 | Success | Pending |
| Guest to camera | Guest ping 10.10.30.10 | Blocked by guest ACL | Pending |

Also check the guest ACL binding with show ip interface g0/0.20 and show access-lists. Guest ping to private addresses, including its gateway, is intentionally denied. Guest DHCP remains allowed.

For each test, capture commands, the observed result, and whether it matches the expectation. Do not fabricate device output.
