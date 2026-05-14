# Lab Overview

This document covers the foundational configuration of the ServiceNow Help Desk Ticketing Lab — SLA policies, user and group setup, dashboard metrics, and overall lab architecture.

---

## Lab Objectives

This lab simulates a Tier 1 help desk and NOC environment within ServiceNow to demonstrate practical IT support skills:

- End-to-end incident lifecycle management
- Service request fulfillment with approval workflows
- SLA tracking and breach analysis
- Knowledge base documentation
- Reporting and dashboard creation
- User and group management

---

## Platform Configuration

- **Instance:** ServiceNow Personal Developer Instance (PDI)
- **Release:** Australia (Latest)
- **Demo Data:** Pre-loaded ACME Corporation dataset (637 users, multiple departments, pre-built groups)
- **UI:** Next Experience (Polaris)

---

## User & Group Management

Three lab users were created to simulate ticket callers across different departments:

| User | Department | Role | Use Case |
|---|---|---|---|
| John Carter | Finance | End User | Software issues, account lockouts |
| Maria Santos | Marketing | End User | Hardware and printer issues |
| David Kim | IT | End User / Reporter | Network incidents, escalations |

**Pre-built groups used for ticket routing:**

- Service Desk — Tier 1 incident assignment
- Network — P1 critical incidents and DNS/connectivity issues
- Network — Hardware fulfillment routing

---

## SLA Configuration

The lab leverages pre-configured SLA definitions on the Incident table. SLAs are automatically attached to tickets based on priority.

| SLA Policy | Type | Duration | Triggers When |
|---|---|---|---|
| Priority 1 resolution | SLA | 1 Hour | Priority = 1 - Critical |
| Priority 1 response | SLA | 15 Minutes | Priority = 1 - Critical |
| Priority 2 resolution | SLA | 8 Hours | Priority = 2 - High |
| Priority 2 response | SLA | 1 Hour | Priority = 2 - High |
| Priority 3 resolution | SLA | 1 Day | Priority = 3 - Moderate |
| Priority 3 response | SLA | 4 Hours | Priority = 3 - Moderate |
| Network group resolution | OLA | 4 Hours | Assignment Group = Network |

**Key SLA settings observed:**

- Schedule: 24x7 (no business hours restriction)
- Retroactive start enabled
- Retroactive pause enabled
- Auto-attaches based on Priority field condition

### SLA Breach Scenario

INC0010003 (Network Outage, P1 Critical) demonstrated a real SLA breach:

- **Priority 1 response SLA (15 minutes):** BREACHED — 3,013% elapsed time
- **Priority 1 resolution SLA (1 hour):** MET — 5.64% elapsed when resolved
- **Network group OLA:** MET — 1.41% elapsed

This breach occurred organically because the ticket was created and worked through over multiple sessions, demonstrating how the 15-minute response SLA can be missed in real-world scenarios where techs are juggling multiple priorities.

---

## Incident Workflow

All incidents followed a standard Tier 1 lifecycle:

1. **New** — Ticket created with caller, category, priority
2. **In Progress** — Work notes documenting investigation
3. **Resolved** — Resolution code and resolution notes added
4. **Closed** — Final state after resolution confirmation

**Categories used:** Software, Hardware, Network, Security
**Channels used:** Phone, Email, Self-service

---

## Service Request Workflow

Service requests followed a multi-stage approval workflow:

1. **Submitted** via Service Catalog
2. **Manager Approval** — automatic approval step
3. **Department Head Approval** — secondary approval for hardware
4. **Order Fulfillment** — IT processes the request
5. **Deployment** — software installed or hardware delivered
6. **Closed Complete** — user confirms receipt

---

## Knowledge Base Setup

Three SOP-style articles published in the IT knowledge base:

| Article | Type | Linked Incident |
|---|---|---|
| KB0010001 - Password Reset SOP | Standard | INC0010001 |
| KB0010002 - DNS Troubleshooting | Standard | INC0010002 |
| KB0010003 - Printer Troubleshooting | Standard | INC0010004 |

Each article follows a consistent format:

- **ISSUE** — what the user reported
- **SYMPTOMS** — observable behavior
- **STEPS TO RESOLVE** — numbered procedure
- **PREVENTION** — long-term mitigation

---

## Reporting & Dashboard

**Custom report built:**

- **Name:** Incidents by Priority
- **Type:** Vertical bar chart
- **Data source:** Incident table
- **Grouped by:** Priority field
- **Aggregation:** Count

**Custom dashboard built:**

- **Name:** NOC - Help Desk Overview
- **Editor:** In-line editor (drag and drop)
- **Visualizations:** Incidents created (by priority) over time

---

## Lab Outcomes

By completing this lab, the following ITSM competencies were demonstrated:

- Configuring incidents with proper categorization and prioritization
- Routing tickets to correct assignment groups
- Documenting resolution paths in work notes
- Recognizing and analyzing SLA breaches
- Creating and publishing knowledge base content
- Building reports and dashboards for operational visibility
- Managing the full ticket lifecycle from creation to closure