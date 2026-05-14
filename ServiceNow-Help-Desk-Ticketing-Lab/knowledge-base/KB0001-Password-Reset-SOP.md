# KB0001 - Password Reset SOP

## Article Summary

| Field | Value |
|---|---|
| **Article Number** | KB0010001 |
| **Knowledge Base** | IT |
| **Template** | Standard |
| **Workflow** | Published |
| **Related Incident** | [INC0001 - Password Reset](../incidents/INC0001-Password-Reset.md) |

---

## Short Description

Password Reset SOP - Account Lockout Resolution

---

## Article Content

### ISSUE

User is locked out of their Windows account after multiple failed login attempts.

### SYMPTOMS

- User cannot log in to Windows workstation
- Error message: "Account is locked out"
- Multiple failed login attempts recorded

### STEPS TO RESOLVE

1. Verify user identity by confirming employee ID and department
2. Navigate to Active Directory Users and Computers
3. Locate the user account
4. Right-click the account and select "Unlock Account"
5. Reset password and set "User must change password at next logon"
6. Communicate temporary password to user via phone
7. Confirm user can log in successfully
8. Document resolution in ServiceNow ticket

### PREVENTION

- Advise user to use password manager to avoid future lockouts
- Remind user of password expiry policy (90 days)

---

## Screenshot

- `screenshots/knowledge-base/KB0001-password-reset.png`