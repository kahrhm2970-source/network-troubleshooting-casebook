# INC-001 — Incorrect Access VLAN

## Status
Pending execution. This is a reproducible runbook, not a completed incident report.

## Preconditions
Build and verify the baseline. Open a separate copy for this case. Introduce only the fault below.

## Fault injection
On SW1:
```text
enable
configure terminal
interface FastEthernet0/1
 switchport access vlan 20
end
```
On Staff PC, reselect DHCP.

## Expected symptoms
Staff may receive a guest VLAN 20 address instead of its intended VLAN 10 address. Guest ACL restrictions can then block internal traffic.

## Investigation
Compare Staff ipconfig with the address plan. Inspect SW1 show vlan brief and show interfaces FastEthernet0/1 switchport. Compare the access VLAN against baseline.

## Planned remediation
On SW1:
```text
configure terminal
interface FastEthernet0/1
 switchport access vlan 10
end
```
Renew Staff DHCP again.

## Expected verification
Staff receives 10.10.10.11–254 /24 with gateway 10.10.10.1 and reaches 10.10.30.10 after ARP.

## Actual evidence and root cause
Pending. Record commands and observed outputs here. Confirm the root cause through evidence before marking it resolved.

## Screenshots
Pending before/after captures in screenshots/. Record their filenames here after execution.

## Lessons learned and prevention
Pending execution. Explain the most informative observation, recovery test, and one preventive action.
