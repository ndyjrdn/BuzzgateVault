### 👤 **User Profile**

- **Name:** Andy
    
- **Location:** Des Moines, Iowa area
    
- **Background:** MBA + Master of Business Analytics
    
- **Technical Skills:** Docker Compose, MariaDB, InfluxDB, Nextcloud, Synology NAS, SSH, ACLs, YAML, PHP, Linux admin, network diagnostics
    
- **Workflow Style:** Modular, version-controlled, YAML-driven, prefers persistent context and stepwise troubleshooting
    

### 🏠 **Smart Home Ecosystem: Buzzgate**

- **Core Goals:**
    
    - Fully local, customizable automation
        
    - Zigbee/Matter mesh reliability
        
    - Scene-based lighting and media control
        
    - Family-friendly access and emergency alerting
        
    - Monitoring + alerting for uptime, WAN speed, zombie processes, etc.
        
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