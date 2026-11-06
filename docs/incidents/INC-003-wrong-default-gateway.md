# INC-003 — Incorrect Default Gateway

## Status
Pending execution. This is a reproducible runbook, not a completed incident report.

## Preconditions
Build and verify the baseline. Open a separate copy for this case. Introduce only the fault below.

## Fault injection
On Camera PC, keep 10.10.30.10/24 but change its gateway from 10.10.30.1 to the unused address 10.10.30.254.

## Expected symptoms
Admin-to-camera ping may fail because the camera cannot return traffic to another subnet.

## Investigation
From Admin PC, ping 10.10.30.10. Check camera IP, mask, and gateway. Compare the gateway against R1 G0/0.30. Do not use Guest as the source because its baseline ACL blocks this destination.

## Planned remediation
Restore Camera PC gateway to 10.10.30.1.

## Expected verification
Admin-to-camera and Staff-to-camera pings succeed after ARP.

## Actual evidence and root cause
Pending. Record commands and observed outputs here. Confirm the root cause through evidence before marking it resolved.

## Screenshots
Pending before/after captures in screenshots/. Record their filenames here after execution.

## Lessons learned and prevention
Pending execution. Explain the most informative observation, recovery test, and one preventive action.
