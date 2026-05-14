# INC0002 - DNS Resolution Failure

## Ticket Summary

| Field | Value |
|---|---|
| **Number** | INC0010002 |
| **Caller** | Maria Santos (Marketing) |
| **Channel** | Phone |
| **Category** | Network |
| **Subcategory** | DNS |
| **Impact** | 2 - Medium |
| **Urgency** | 2 - Medium |
| **Priority** | 3 - Moderate |
| **Assignment Group** | Network |
| **State** | Resolved |
| **Resolution Code** | Solution provided |

---

## Short Description

User unable to resolve internal DNS - cannot access company intranet

## Description

Maria Santos from Marketing reports she cannot access internal company websites since this morning. Browser returns DNS_PROBE_FINISHED_NXDOMAIN error. Other users on same floor reporting similar issue. Possible DNS server failure affecting Marketing department.

---

## Work Notes

Received report from Maria Santos, Marketing. Multiple users affected on same floor. Ran nslookup - DNS server not responding. Escalated to Network team. Network team confirmed DNS service restart required. DNS service restarted on primary server. Verified resolution - users confirmed access restored. Ticket resolved.

---

## Resolution

DNS service restarted on primary server. All affected users confirmed access restored. Monitored for 15 minutes post-fix with no reoccurrence.

---

## Related KB Article

- [KB0002 - DNS Troubleshooting](../knowledge-base/KB0002-DNS-Troubleshooting.md)

---

## Screenshots

- `screenshots/incidents/INC0002-filled-form.png`
- `screenshots/incidents/INC0002-work-notes.png`
- `screenshots/incidents/INC0002-resolved.png`