# Port Cheatsheet — SOC Analyst Quick Reference

> Every SOC analyst knows these cold. Memorize them.

| PORT | PROTOCOL | RISK LEVEL | SOC RELEVANCE |
|------|----------|------------|---------------|
| 21 | FTP | HIGH | Unencrypted file transfer — data exfil risk |
| 22 | SSH | HIGH | Remote Linux access — brute force target |
| 23 | Telnet | CRITICAL | Unencrypted — should NEVER be open |
| 25 | SMTP | HIGH | Email — phishing delivery vector |
| 53 | DNS | HIGH | C2 communication, DNS tunneling/exfiltration |
| 80 | HTTP | MEDIUM | Web traffic — unencrypted, inspect payloads |
| 443 | HTTPS | INFO | Web traffic — encrypted, check cert validity |
| 445 | SMB | CRITICAL | Windows file sharing — lateral movement (WannaCry/EternalBlue) |
| 3389 | RDP | CRITICAL | Remote Desktop — brute force target, ransomware entry |
| 8080 | HTTP-alt | HIGH | Web proxy, C2 traffic, web shells |
| 4444 | Metasploit | CRITICAL | Default C2/reverse shell — incident confirmed if seen |
| 1433 | MSSQL | HIGH | Database — SQL injection target |

---

## Risk Level Key

- 🔴 **CRITICAL** — Immediate investigation required
- 🟠 **HIGH** — Suspicious, correlate with other indicators
- 🟡 **MEDIUM** — Worth monitoring in context
- 🔵 **INFO** — Normal traffic, but can hide threats

---

## Quick Memory Tips

- **21, 22, 23** — File transfer & remote access trio
- **25, 53** — Email & DNS (both abused for C2/exfil)
- **80, 443, 8080** — Web traffic family
- **445, 3389** — Windows attack surface
- **4444** — See this? Call your SOC lead NOW

---

*Day 02 — Networking Basics | SOC Analyst Portfolio by Codexanandh*
