# SecureShell-Analyzer
# 🛡️ SecureShell Analyzer

> **AI-powered cybersecurity log analyzer with real-time threat detection**

A browser-based security tool that uses **Claude AI** to analyze server logs and network traffic for threats, built by **Ravi Kumawat**.

![SecureShell Analyzer](https://img.shields.io/badge/Status-Live-00ff88?style=flat-square&labelColor=050a05)
![AI Powered](https://img.shields.io/badge/AI-Claude%20Sonnet-bb88ff?style=flat-square&labelColor=050a05)
![Language](https://img.shields.io/badge/Language-HTML%20%2F%20JS-44aaff?style=flat-square&labelColor=050a05)
![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-ff4455?style=flat-square&labelColor=050a05)

---

## 🚀 Live Demo

👉 [Open SecureShell Analyzer](https://your-username.github.io/secureshell-analyzer)

---

## 📸 Features

| Feature | Description |
|---|---|
| ⚡ AI Analysis | Claude AI reads logs and identifies attack types |
| 🔴 Threat Detection | Flags SSH brute force, DDoS, SQLi, port scans |
| 📊 Risk Score | 0–100 risk score with visual indicator |
| 🌐 IP Scanner | Detects and classifies suspicious IPs |
| 📄 Export Report | Download full threat report as `.txt` |
| 💻 Terminal UI | Hacker-style terminal with live output |
| 🧪 5 Sample Attacks | Pre-loaded real-world attack scenarios |
| ⌨️ CLI Commands | Built-in command interface (`help`, `scan`, `whois`, etc.) |

---

## 🔍 Supported Attack Types

1. **SSH Brute Force** — Repeated failed login attempts
2. **Port Scanning** — Systematic port enumeration (reconnaissance)
3. **DDoS SYN Flood** — Massive SYN packet flooding
4. **SQL Injection** — Malicious SQL via HTTP requests
5. **Normal Traffic** — Baseline comparison scenario



---

## 📝 Example Logs to Paste

### SSH Brute Force Attack:
```
Nov 16 08:11:42 server sshd[1234]: Failed password for root from 192.168.1.105 port 43210 ssh2
Nov 16 08:11:43 server sshd[1234]: Failed password for root from 192.168.1.105 port 43211 ssh2
Nov 16 08:11:44 server sshd[1234]: Failed password for admin from 192.168.1.105 port 43212 ssh2
Nov 16 08:11:45 server sshd[1234]: Failed password for ubuntu from 192.168.1.105 port 43213 ssh2
Nov 16 08:11:46 server sshd[1234]: Failed password for root from 192.168.1.105 port 43214 ssh2
Nov 16 08:11:47 server sshd[1235]: Accepted password for deploy from 10.0.0.5 port 22 ssh2
```

### Port Scan Detection:
```
2026-05-16 09:00:01 SYN 203.0.113.42:54321 -> 10.0.0.1:22 [SSH]
2026-05-16 09:00:01 SYN 203.0.113.42:54322 -> 10.0.0.1:80 [HTTP]
2026-05-16 09:00:01 SYN 203.0.113.42:54323 -> 10.0.0.1:3306 [MySQL] BLOCKED
2026-05-16 09:00:01 SYN 203.0.113.42:54324 -> 10.0.0.1:5432 [Postgres] BLOCKED
2026-05-16 09:00:01 SYN 203.0.113.42:54325 -> 10.0.0.1:6379 [Redis] BLOCKED
```

### SQL Injection:
```
2026-05-16 11:22:01 "GET /login?user=admin'--&pass=x HTTP/1.1" 200 "sqlmap/1.7"
2026-05-16 11:22:02 "GET /search?q=' OR 1=1-- HTTP/1.1" 500 "sqlmap/1.7"
2026-05-16 11:22:03 "GET /product?id=1 UNION SELECT username,password FROM users-- HTTP/1.1" 200
```

---

## ⌨️ Terminal Commands

| Command | Description |
|---|---|
| `help` | Show all commands |
| `scan` | Run AI analysis on loaded logs |
| `status` | Show current threat counts |
| `clear` | Clear the terminal |
| `export` | Download threat report |
| `ips` | List all detected IPs |
| `whois [ip]` | Look up IP information |
| `tips` | Show security recommendations |

---

## 🔐 Security Recommendations (from the tool)

- **SSH:** Disable root login, use key-based authentication, deploy `fail2ban`
- **Ports:** Use firewall rules (`ufw`/`iptables`), close all unused ports
- **DDoS:** Implement rate limiting, use Cloudflare or edge protection
- **SQLi:** Always use parameterized queries, never trust user input
- **General:** Monitor logs daily, set up alerts with SIEM tools

---

## 📂 Project Structure

```
secureshell-analyzer/
├── index.html      # Complete single-file application
├── README.md       # This file
└── examples/
    └── sample-logs.txt   # Example logs for testing
```

---

## 🤝 Contributing

Pull requests welcome! Ideas for improvement:
- [ ] Python backend for reading real `.log` files
- [ ] IP geolocation map visualization
- [ ] Real-time log streaming (WebSocket)
- [ ] More attack signature patterns
- [ ] Dark/Light theme toggle

---

## 📄 License

MIT License — free to use, modify, and distribute.

---
