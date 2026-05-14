# INC0003 - Network Outage (P1 Critical)

## Ticket Summary

| Field | Value |
|---|---|
| **Number** | INC0010003 |
| **Caller** | David Kim (IT) |
| **Channel** | Phone |
| **Category** | Network |
| **Subcategory** | (none) |
| **Impact** | 1 - High |
| **Urgency** | 1 - High |
| **Priority** | 1 - Critical |
| **Assignment Group** | Network |
| **State** | Resolved |
| **Resolution Code** | Solution provided |

---

## Short Description

Complete network outage - Floor 3 users cannot access network resources

## Description

David Kim, IT department, reports complete network outage affecting all users on Floor 3. Users cannot access shared drives, intranet, or internet. Approximately 45 users impacted. Issue began at 16:00. Potential switch or router failure. Immediate escalation required.

---

## Work Notes

P1 Major incident declared. All Floor 3 users confirmed down. Contacted Network team and escalated to senior engineer. Physical inspection of server room initiated. Core switch found unresponsive - power cycled. Switch came back online at 16:45. Network connectivity restored to all Floor 3 users. Monitored for 30 minutes - stable. Incident resolved. Post-incident review scheduled.

---

## Resolution

Core network switch on Floor 3 was unresponsive. Power cycle performed by Network Engineer. Full connectivity restored to all 45 affected users. Total downtime 45 minutes. PIR scheduled.

---

## SLA Analysis

This P1 incident triggered three SLA timers, providing a real-world example of both SLA success and breach:

| SLA Policy | Type | Target | Result |
|---|---|---|---|
| Priority 1 resolution | SLA | 1 Hour | MET (5.64% elapsed) |
| Priority 1 response | SLA | 15 Minutes | BREACHED (3,013% elapsed) |
| Network group resolution | OLA | 4 Hours | MET (1.41% elapsed) |

The response SLA was breached because initial response exceeded the 15-minute target. This is a realistic scenario in Tier 1 environments where techs juggle multiple priorities simultaneously.

---

## Screenshots

- `screenshots/incidents/INC0003-filled-form.png`
- `screenshots/incidents/INC0003-work-notes.png`
- `screenshots/incidents/INC0003-resolved.png`
- `screenshots/sla/03-p1-ticket-sla.png` (SLA breach evidence)
