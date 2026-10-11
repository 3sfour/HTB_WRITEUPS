# <Box Name>

| | |
|---|---|
| **OS** | Linux / Windows / Other |
| **Difficulty** | Easy / Medium / Hard / Insane |
| **Release date** | YYYY-MM-DD |
| **Retired** | Yes (confirm before publishing) |
| **Date solved** | YYYY-MM-DD |
| **Tags** | e.g. web, SQLi, kerberoasting, sudo |

## Summary
Two or three sentences: what the box is about and the attack path from foothold to root.

## Attack path
1. Foothold: ...
2. User: ...
3. Root: ...

## Recon

### Port scan
```
nmap -sC -sV -p- <TARGET_IP>
```
Paste relevant output. Note what stands out.

### Enumeration
Web content discovery, SMB shares, DNS, LDAP, etc. Explain what you looked for and why.

## Foothold
- **Vulnerability:**
- **Root cause:**
- **Exploitation steps:**

```
commands here
```

## User
How you moved from the foothold shell to the user account.

**user.txt:** `[REDACTED]`

## Privilege escalation
- **Vulnerability / misconfiguration:**
- **Root cause:**
- **Steps:**

```
commands here
```

**root.txt:** `[REDACTED]`

## Lessons learned
- What new technique or tool did I pick up?
- What did I get stuck on, and what unblocked me?

## Remediation
How each vulnerability should be fixed.

## References
- Tools used:
- Articles / research:
