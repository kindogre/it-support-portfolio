# KB0002 - DNS Troubleshooting

## Article Summary

| Field | Value |
|---|---|
| **Article Number** | KB0010002 |
| **Knowledge Base** | IT |
| **Template** | Standard |
| **Workflow** | Published |
| **Related Incident** | [INC0002 - DNS Resolution Failure](../incidents/INC0002-DNS-Resolution-Failure.md) |

---

## Short Description

DNS Troubleshooting - Unable to Resolve Internal Sites

---

## Article Content

### ISSUE

User cannot access internal company websites or intranet. Browser returns DNS_PROBE_FINISHED_NXDOMAIN error.

### SYMPTOMS

- Internal websites not loading
- DNS error in browser
- Other users on same network affected
- External sites may still work

### STEPS TO RESOLVE

1. Ask user to open Command Prompt
2. Run: `ipconfig /flushdns`
3. Run: `nslookup [internal site name]`
4. If DNS server not responding, escalate to Network team
5. Network team to restart DNS service on primary server
6. Verify resolution: `ping [internal site name]`
7. Confirm user can access intranet
8. Document steps in ServiceNow ticket

### PREVENTION

- Monitor DNS server health via NOC dashboard
- Set up alerts for DNS service failures

---

## Screenshot

- `screenshots/knowledge-base/KB0002-dns-troubleshooting.png`