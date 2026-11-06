# INC-002 — Missing Trunk VLAN

## Status
Pending execution. This is a reproducible runbook, not a completed incident report.

## Preconditions
Build and verify the baseline. Open a separate copy for this case. Introduce only the fault below.

## Fault injection
On SW1:
```text
enable
configure terminal
interface GigabitEthernet0/1
 switchport trunk allowed vlan remove 10
end
```

## Expected symptoms
Staff loses routed connectivity. A fresh Staff DHCP request may also fail.

## Investigation
Keep an existing Staff lease when testing connectivity, or record DHCP failure separately. Compare show interfaces trunk with baseline. Check router show ip interface brief and switch VLAN membership to distinguish trunk filtering from an access-port fault.

## Planned remediation
On SW1:
```text
configure terminal
interface GigabitEthernet0/1
 switchport trunk allowed vlan add 10
end
```

## Expected verification
VLAN 10 is allowed across the trunk. Staff DHCP and ping to 10.10.30.10 work after renewal/ARP as appropriate.

## Actual evidence and root cause
Pending. Record commands and observed outputs here. Confirm the root cause through evidence before marking it resolved.

## Screenshots
Pending before/after captures in screenshots/. Record their filenames here after execution.

## Lessons learned and prevention
Pending execution. Explain the most informative observation, recovery test, and one preventive action.
