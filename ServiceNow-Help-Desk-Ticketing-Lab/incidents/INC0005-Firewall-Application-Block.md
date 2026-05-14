# INC0005 - Firewall Application Block

## Ticket Summary

| Field | Value |
|---|---|
| **Number** | INC0010005 |
| **Caller** | John Carter (Finance) |
| **Channel** | Self-service |
| **Category** | Network |
| **Subcategory** | (none) |
| **Impact** | 2 - Medium |
| **Urgency** | 2 - Medium |
| **Priority** | 3 - Moderate |
| **Assignment Group** | Network |
| **State** | Resolved |
| **Resolution Code** | Solution provided |

---

## Short Description

Business application blocked by firewall - user cannot access Zoom

## Description

John Carter from Finance submitted a self-service ticket reporting he is unable to access Zoom for a scheduled client call. Application times out on launch. Other users in Finance reporting the same issue. Suspected firewall rule blocking application traffic after recent security policy update.

---

## Work Notes

Received self-service ticket from John Carter, Finance. Multiple Finance users unable to access Zoom. Verified connectivity to other sites - working normally. Isolated issue to Zoom application traffic. Escalated to Network Security team. Team confirmed recent firewall policy update blocked Zoom traffic on port 443. Exception rule created for Finance department. Zoom access restored and verified with John Carter. Ticket resolved.

---

## Resolution

Firewall policy update confirmed blocking Zoom application traffic. Network Security team created firewall exception rule for Finance department on port 443. All affected users confirmed Zoom access restored.

---

## Screenshots

- `screenshots/incidents/INC0005-filled-form.png`
- `screenshots/incidents/INC0005-work-notes.png`
- `screenshots/incidents/INC0005-resolved.png`