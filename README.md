# 🐾 Neko Net
*A self-hosted synchronization server for Final Fantasy XIV (Mare Synchronos replacement)*  


---

## ✨ Features
- 🔒 **Secure sync** of modded assets between FFXIV players  
- 🐾 **Re-branded and maintained** fork of Mare Synchronos under the Neko Net umbrella  
- ⚡ **Docker-based deployment** for quick setup  
- 📦 **Standalone or sharded modes** depending on scale  
- 🤖 **Discord bot integration** for account verification  
- 📂 **Optimized file delivery** via Nginx with CDN/Cache support  

---

## 📋 Requirements
- Linux server (Ubuntu 22.04/24.04 LTS recommended)  
- Docker & Docker Compose installed  
- PostgreSQL and Redis (deployed automatically via Docker)  
- Domain name with SSL (via Let’s Encrypt)  
- (Optional) Discord Application & Bot Token  

---

## 🚀 Quick Start (Standalone)
```bash
# 1. Clone the repository
git clone https://github.com/your-org/neko-net.git
cd neko-net/Docker

# 2. Configure environment
cp compose/.env.example compose/.env
# edit DEV_MARE_CDNURL, DEV_MARE_DISCORDTOKEN, etc.

# 3. Build and run containers
docker compose -f compose/docker-compose.standalone.yml up -d

# 4. Check logs
docker compose logs -f
