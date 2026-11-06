# Baseline setup
Status: pending Packet Tracer execution.

1. Create one Cisco 2911, one Catalyst 2960, and four PCs.
2. Wire R1 G0/0 to SW1 G0/1 with Copper Straight-Through.
3. Wire Staff to Fa0/1, Guest to Fa0/2, Camera PC to Fa0/3, Admin to Fa0/4.
4. Open router CLI and paste configs/baseline/router.cfg. Open switch CLI and paste configs/baseline/switch.cfg. Accept the default save filename if prompted.
5. Select DHCP on Staff and Guest Desktop > IP Configuration.
6. Configure Camera PC 10.10.30.10 / 255.255.255.0 / gateway 10.10.30.1.
7. Configure Admin PC 10.10.99.10 / 255.255.255.0 / gateway 10.10.99.1.
8. Wait for links and ARP to settle, run verification.md, then save labs/baseline.pkt.
9. Record Packet Tracer version, date, and actual evidence. Preserve the baseline and use copies for fault scenarios.

CLI files target fresh simulation devices. They are not device backup files for direct production deployment.
