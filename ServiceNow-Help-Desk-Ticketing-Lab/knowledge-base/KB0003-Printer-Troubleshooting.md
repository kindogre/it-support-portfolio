# KB0003 - Printer Troubleshooting

## Article Summary

| Field | Value |
|---|---|
| **Article Number** | KB0010003 |
| **Knowledge Base** | IT |
| **Template** | Standard |
| **Workflow** | Published |
| **Related Incident** | [INC0004 - Printer Offline](../incidents/INC0004-Printer-Offline.md) |

---

## Short Description

Printer Troubleshooting - Shared Office Printer Offline

---

## Article Content

### ISSUE

Shared office printer showing offline status. Users unable to print documents.

### SYMPTOMS

- Printer shows offline in Windows devices
- Print jobs stuck in queue
- Other users on same floor affected
- Printer power light is on

### STEPS TO RESOLVE

1. Check printer power and cable connections
2. Reseat USB or network cable on printer
3. On print server open Services
4. Locate Print Spooler service
5. Right-click and select Restart
6. Clear print queue - delete all stuck jobs
7. Print a test page to confirm
8. Confirm with user that printing is restored
9. Document resolution in ServiceNow ticket

### PREVENTION

- Schedule monthly print spooler maintenance
- Check printer cable connections during quarterly hardware audits

---

## Screenshot

- `screenshots/knowledge-base/KB0003-printer-troubleshooting.png`