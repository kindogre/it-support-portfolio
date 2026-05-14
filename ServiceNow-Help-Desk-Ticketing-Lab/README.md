# ServiceNow Help Desk Ticketing Lab

A hands-on IT help desk simulation built on a ServiceNow Personal Developer Instance (PDI). This lab demonstrates real Tier 1 and NOC workflows including incident management, service request fulfillment, SLA tracking, knowledge base authoring, and reporting.

---

## Tools & Platform

- **Platform:** ServiceNow (Australia Release — Latest)
- **Instance Type:** Personal Developer Instance (PDI)
- **Concepts:** ITIL v4, Incident Management, Service Request Fulfillment, SLA Management, Knowledge-Centered Service (KCS)

---

## What I Built

- Created and resolved **5 incidents** spanning network, hardware, software, and security categories
- Fulfilled **2 service requests** through the Service Catalog with approval workflows
- Authored **3 knowledge base articles** linked to resolved incidents
- Configured and analyzed **SLA policies** including a real P1 SLA breach scenario
- Built a **NOC dashboard** tracking incident volume by priority
- Managed **users, groups, and assignment routing**

---

## Incident Scenarios

| Ticket | Category | Priority | Caller | Channel |
|---|---|---|---|---|
| INC0010001 - Password Reset | Software | 3 - Moderate | John Carter | Phone |
| INC0010002 - DNS Resolution Failure | Network | 3 - Moderate | Maria Santos | Phone |
| INC0010003 - Network Outage (P1) | Network | 1 - Critical | David Kim | Phone |
| INC0010004 - Printer Offline | Hardware | 4 - Low | Maria Santos | Email |
| INC0010005 - Firewall Application Block | Network | 3 - Moderate | John Carter | Self-service |

### Incident Lifecycle — INC0010001 Password Reset

**Filled incident form:**

![INC0001 Filled Form][inc1-form]

**Work notes documenting resolution steps:**

![INC0001 Work Notes][inc1-notes]

**Resolved with resolution code and notes:**

![INC0001 Resolved][inc1-resolved]

---

## Service Requests

| Request | Item | Requested For | Outcome |
|---|---|---|---|
| REQ0010003 - Software Install | Adobe Acrobat | John Carter | Closed Complete |
| REQ0010004 - Hardware Request | Lenovo Carbon x1 Laptop | Maria Santos | Closed Complete |

**Service Catalog:**

![Service Catalog][catalog]

**REQ0002 multi-stage approval workflow (Manager Approval → Dept Head → Order Fulfillment → Deployment):**

![REQ0002 Approval Workflow][req2-workflow]

**REQ0002 closed and fulfilled:**

![REQ0002 Closed][req2-closed]

---

## Knowledge Base Articles

| Article | Linked To |
|---|---|
| KB0010001 - Password Reset SOP | INC0010001 |
| KB0010002 - DNS Troubleshooting | INC0010002 |
| KB0010003 - Printer Troubleshooting | INC0010004 |

![KB0001 Password Reset SOP][kb1]

---

## SLA Configuration & Breach Analysis

ServiceNow SLA definitions were applied across all incidents based on priority level.

| SLA Policy | Type | Duration | Applies To |
|---|---|---|---|
| Priority 1 resolution | SLA | 1 Hour | P1 Critical |
| Priority 1 response | SLA | 15 Minutes | P1 Critical |
| Priority 2 resolution | SLA | 8 Hours | P2 High |
| Priority 3 resolution | SLA | 1 Day | P3 Moderate |

**Full SLA definitions list:**

![SLA Definitions List][sla-list]

**P1 Resolution SLA definition (1 hour, conditions, start triggers):**

![P1 SLA Definition][sla-p1]

### Live SLA Breach — INC0010003 Network Outage

The P1 response SLA (15 minutes) was breached on the network outage ticket, visible in the Task SLA panel with a 3,013% elapsed percentage and red breach indicator.

![SLA Breach on P1 Ticket][sla-breach]

---

## Reports & Dashboard

Built an **Incidents by Priority** report and added it to a custom **NOC - Help Desk Overview** dashboard.

**Incidents by Priority bar chart:**

![Incidents by Priority Report][report]

**NOC Dashboard with embedded visualization:**

![NOC Dashboard][dashboard]

---

## User Management

| User | Department | Role |
|---|---|---|
| John Carter | Finance | End User |
| Maria Santos | Marketing | End User |
| David Kim | IT | End User / Reporter |

![All Lab Users][users]

---

## Skills Demonstrated

| Skill | Evidence |
|---|---|
| Incident Management | 5 incidents created, worked, and resolved with full lifecycle documentation |
| Service Request Fulfillment | 2 catalog requests fulfilled through approval workflow |
| SLA Management | P1 SLA definitions reviewed, breach identified and documented |
| Knowledge Base Authoring | 3 KB articles written and published in IT knowledge base |
| Reporting & Dashboards | Custom report and NOC dashboard built |
| User & Group Management | Users created and assigned to tickets with correct routing |
| ITIL v4 Concepts | Incident vs Request distinction, escalation paths, resolution codes |
| Documentation | All tickets documented with work notes, resolution notes, and channel tracking |

---

## Repository Structure

```
ServiceNow-Help-Desk-Ticketing-Lab/
├── README.md
├── docs/
│   ├── Lab-Overview.md
│   └── Skills-Matrix.md
├── incidents/
│   ├── INC0001-Password-Reset.md
│   ├── INC0002-DNS-Resolution-Failure.md
│   ├── INC0003-Network-Outage.md
│   ├── INC0004-Printer-Offline.md
│   └── INC0005-Firewall-Application-Block.md
├── service-requests/
│   ├── REQ0001-Software-Installation.md
│   └── REQ0002-Hardware-Request.md
├── knowledge-base/
│   ├── KB0001-Password-Reset-SOP.md
│   ├── KB0002-DNS-Troubleshooting.md
│   └── KB0003-Printer-Troubleshooting.md
└── screenshots/
    ├── incidents/
    ├── knowledge-base/
    ├── reports/
    ├── service-requests/
    ├── sla/
    └── user-management/
```

---

*Built on ServiceNow PDI — Australia Release | 2026*


[inc1-form]: screenshots/incidents/INC0001-filled-form.png
[inc1-notes]: screenshots/incidents/INC0001-work-notes.png
[inc1-resolved]: screenshots/incidents/INC0001-resolved.png
[catalog]: screenshots/service-requests/00-service-catalog.png
[req2-workflow]: screenshots/service-requests/REQ0002-approval-workflow.png
[req2-closed]: screenshots/service-requests/REQ0002-closed.png
[kb1]: screenshots/knowledge-base/KB0001-password-reset.png
[sla-list]: screenshots/sla/01-sla-definitions-list.png
[sla-p1]: screenshots/sla/02-p1-sla-definition.png
[sla-breach]: screenshots/sla/03-p1-ticket-sla.png
[report]: screenshots/reports/01-incidents-by-priority.png
[dashboard]: screenshots/reports/02-noc-dashboard.png
[users]: screenshots/user-management/04-all-lab-users.png