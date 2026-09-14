# 🏠 Turnstile Solver Wiki

> **Self-hosted Cloudflare Turnstile solver with proxy rotation and 2Captcha fallback**

## 📚 Navigation

| Section | Description |
|---------|-------------|
| [Installation](guides/installation.md) | Step-by-step setup guide |
| [Proxy Management](guides/proxy-management.md) | How to manage and refresh proxies |
| [API Reference](api/reference.md) | Complete API documentation |
| [Troubleshooting](troubleshooting/common-issues.md) | Fix common problems |
| [Development](development/contributing.md) | Contribute to the project |

## 🚀 Quick Start

```bash
# Clone and start
git clone https://github.com/marktantongco/turnstile-solver.git
cd turnstile-solver
sudo docker compose -f docker-compose.override.yml up -d

# Verify
curl -H "secret: turnstile123" http://localhost:8088/
```

## 📊 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| RAM | 2GB | 4GB |
| CPU | 2 cores | 4 cores |
| Disk | 5GB | 10GB |
| Docker | 20.10+ | Latest |

---

## 🔗 Ecosystem Links

### Core Stack

| Repository | Description | Status |
|------------|-------------|--------|
| [ai-gateway-complete](https://github.com/marktantongco/ai-gateway-complete) | Full-stack combined repo | ✅ Active |
| [ai-gateway-stack](https://github.com/marktantongco/ai-gateway-stack) | Meta-repo linking all components | ✅ Active |

### Individual Components

| Repository | Language | Description |
|------------|----------|-------------|
| [blacklisted-ai-proxy](https://github.com/marktantongco/blacklisted-ai-proxy) | Node.js | Web UI + API gateway |
| [grokbuild-proxy](https://github.com/marktantongco/grokbuild-proxy) | Go | Grok API proxy + multi-account |
| [turnstile-solver](https://github.com/marktantongco/turnstile-solver) | Python | Cloudflare Turnstile solver |
| [grok-register](https://github.com/marktantongco/grok-register) | Python | Account registration + OAuth |

### Infrastructure

| Repository | Language | Description |
|------------|----------|-------------|
| [thermoptic](https://github.com/marktantongco/thermoptic) | Python | Shared egress proxy (MITM) |
| [phantomsignal](https://github.com/marktantongco/phantomsignal) | Python | Analytics + monitoring |
| [workstation-backup](https://github.com/marktantongco/workstation-backup) | Shell | Full ecosystem backup |

---

## 🌳 Worktree Structure

```
/home/x3/workspace/
├── ai-gateway-complete/          # Main combined repo
│   ├── components/
│   │   ├── blacklisted-ai-proxy/
│   │   ├── grokbuild-proxy/
│   │   ├── turnstile-solver/
│   │   └── grok-register/
│   ├── config/
│   ├── scripts/
│   └── docs/
├── ai-gateway-stack/             # Meta-repo
├── BlacklistedAIProxy/           # Standalone
├── grokbuild-proxy/              # Standalone
├── turnstile_solver/             # Standalone
├── grok-register/                # Standalone
├── Thermoptic/                   # Standalone
└── workstation-backup/           # Backup repo
```

---

## 🔌 Ports Reference

| Port | Service | Protocol | Description |
|------|---------|----------|-------------|
| 3005 | BlacklistedAIProxy | HTTP | Main API endpoint |
| 8090 | GrokBuild Proxy | HTTP | Grok API proxy |
| 8088 | Turnstile Solver | HTTP | Turnstile solving |
| 1234 | Thermoptic | HTTP | Shared egress proxy |
| 14111 | Thermoptic | HTTPS | Secure egress |

---

## 🔗 Links

- [GitHub Repository](https://github.com/marktantongco/turnstile-solver)
- [Docker Hub](https://hub.docker.com/r/marktantongco/turnstile-solver)
- [Issue Tracker](https://github.com/marktantongco/turnstile-solver/issues)
- [Full Documentation](https://github.com/marktantongco/ai-gateway-complete/tree/main/docs)
