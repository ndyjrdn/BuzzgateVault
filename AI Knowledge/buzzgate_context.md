 👤 **User Profile**

- **Name:** Andy
    
- **Location:** Des Moines, Iowa area
    
- **Background:** MBA + Master of Business Analytics
    
- **Technical Skills:** Docker Compose, MariaDB, InfluxDB, Nextcloud, Synology NAS, SSH, ACLs, YAML, PHP, Linux admin, network diagnostics
    
- **Workflow Style:** Modular, version-controlled, YAML-driven, prefers persistent context and stepwise troubleshooting

	## github: 
	project 	
	https://github.com/ndyjrdn/buzzgate
	 Obsidian vault 
	 https://github.com/ndyjrdn/BuzzgateVault

### 🏠 **Smart Home Ecosystem: Buzzgate**

- **Core Goals:**
    
    - Fully local, customizable automation
        
    - Zigbee/Matter mesh reliability
        
    - Scene-based lighting and media control
        
    - Family-friendly access and emergency alerting
        
    - Monitoring + alerting for uptime, WAN speed, zombie processes, etc.
    - 
    ##  Buzzgate Context

Buzzgate is a fully local smart home ecosystem built on Zigbee 3.0, MQTT, and modular YAML automations. It uses a Beelink mini PC ("Brain") to orchestrate containers for monitoring, alerting, and scene control. Key components include:

- Zigbee2MQTT with TubeZB coordinator
- Mosquitto MQTT broker
- Home Assistant with custom scenes and automations
- Glances for system vitals (CPU, memory, disk, zombie processes)
- Grafana + InfluxDB for WAN speed and time-series monitoring
- Alertmanager for modular notifications (Pushover preferred)
- NAS-mounted volumes for persistent memory and media
- Git-backed Obsidian vault for logs, planning, and scene design

Naming conventions follow a Cyclone-themed schema (e.g. `cy-ai`, `BuzzgateVault`, `Skippy`, `Brain`). YAML workflows are modular, versioned, and designed for maintainability.

Recent upgrades include:
- Migration from MariaDB to InfluxDB for monitoring
- Scene refactors for mesh reliability
- Integration of Nextcloud calendars with Home Assistant
        
- **Key Components:**
    
    - **Brain:** Beelink mini PC running Docker containers
        
    - **BuzzgateVault:** Git-backed Obsidian vault for project tracking
        
    - **Buzzgate Monitor:** Grafana + InfluxDB + Glances + Alertmanager
        
    - **Lighting Grid:** Zigbee2MQTT with TubeZB coordinator
        
    - **Media:** Jellyfin integration, retro gaming setups, calendar modding
        

### 🔧 **Recent Projects & Fixes**

- Migrated WAN speed monitoring from MariaDB to InfluxDB
    
- Debugged Alertmanager delivery (SMS → email → push)
    
- Refactored YAML automations for maintainability
    
- Integrated Nextcloud calendars with Home Assistant
    
- Containerized SimTower with LAN-accessible saves
    
- Built backup messaging dashboard for family resilience
    

### 🧩 **Challenges & Quirks**

- Zigbee mesh instability from legacy fixtures
    
- YAML template errors and entity mismatches
    
- DNS and proxy issues with Nginx Proxy Manager
    
- Glances REST API schema changes
    
- LightDM suspend events interfering with uptime tracking
    

### 📈 **Short-Term Goals**

- Scaffold Buzzgate Monitor views (uptime, capacity, errors)
    
- Wire up Glances REST sensors for Brain vitals
    
- Replace ceiling fixture for Zigbee bulb integration
    
- Automate motion detection with time-window logic
    
- Build cAdvisor + Alertmanager stack for container metrics
    

### 🧭 **Long-Term Goals**

- Seamless local-first automation across lighting, media, and storage
    
- Future-proof Zigbee/Matter mesh
    
- Self-hosted LLM as sysadmin assistant
    
- Modular project tracking with LLM-powered planning
    
- LAN-accessible retro gaming with persistent saves

🥽 **IP Addresses and ports**



| Device            | IP Address    | Notes                 |     |
| ----------------- | ------------- | --------------------- | --- |
| Router            | 192.168.1.1   | Default gateway       |     |
| NAS               | 192.168.1.3   | Synology main storage |     |
| Buzzgate Brain    | 192.168.1.177 | Beelink mini PC       |     |
| Pi-hole           | 192.168.1.177 | DNS filtering         |     |
| Zigbee Coord      | 192.168.1.171 | TubeZB USB stick      |     |
|                   |               |                       |     |
| Service/Container |               | container name        |     |
| HomeAssistant     | 8123          | cy-ha                 |     |
| ollama            | 11434         | cy-ai-ollama          |     |
| open-webui        | 6996          | cy-ai-webui           |     |
| whisper           | 10300         | cy-ai-whisper         |     |
| piper             | 10200         | cy-ai-piper           |     |
| glances           | 61208         | glances               |     |
| node-exporter     | 9100          | node-exporter         |     |
| prometheus        | 9090          | prometheus            |     |
| cadvisor          | 8180          | cadvisor              |     |
| grafana           | 3000          | grafana               |     |
| alertmanager      | 9093          | alertmanager          |     |
| wireguard         | 51820         | cy-vpn                |     |
| mosquitto         | 1883          | cy-mosquitto-z2m      |     |
| z2m-lite          | 4242          | cy-mosquitto-z2m      |     |
| nextcloud         | 8081          | cycloud               |     |
| pi-hole           | 8080          | cyhole                |     |
| portainer         | 9000          | portainer             |     |
**Network**
  networks:
  compose_cynet:
    external: true