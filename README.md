🌿 Green AI Lab
<div align="center">
Enterprise-grade cloud and AI infrastructure built from e-waste

Demonstrating sustainable, secure, and scalable architecture practices

Status: 🟢 Active Development | Phase: 2 of 7 | Platform: Ubuntu 24.04 LTS

Architecture • Roadmap • Documentation • Contact

</div>
📖 Overview
Green AI Lab is a production-ready demonstration of cloud-native infrastructure and AI deployment practices using 100% recycled hardware and open-source software. This project showcases enterprise DevOps, security-first architecture, and sustainable technology practices while maintaining zero software licensing costs.

🎯 Project Goals
Replace Commercial Cloud Services → Self-hosted alternatives to Google Workspace, AWS, Netflix
Deploy Private AI Infrastructure → On-premise LLMs and ML workloads with full data sovereignty
Demonstrate Professional DevOps Practices → IaC, CI/CD, containerization, monitoring, security hardening
Minimize Environmental Impact → E-waste reduction, energy efficiency, sustainable computing
Build Career Portfolio → Document real-world cloud architecture and AI infrastructure skills
💼 Business Value Proposition
This project demonstrates skills directly applicable to:

Cloud Architecture → Multi-service orchestration, network design, security implementation
AI/ML Infrastructure → Model deployment, inference optimization, resource management
DevOps Engineering → Automation, IaC, container orchestration, monitoring
Security Engineering → Zero-trust architecture, encryption, access control, compliance
Cost Optimization → Resource efficiency, open-source alternatives, TCO reduction
🏗️ Architecture
System Overview
Network Architecture:

Internet/WAN
    ↓
T-Mobile Router (Firewall)
    ↓
    ├── Node 1 (HP Notebook) - Ubuntu Server - Cloud Services
    ├── Node 2 (Surface Book) - Windows 11 - Management
    ├── APC UPS ES 650 - Power Protection
    └── Future Nodes - Expansion Ready
Technology Stack
Infrastructure Layer
Operating System: Ubuntu Server 24.04 LTS
Networking: Netplan (networkd), WireGuard VPN
Containerization: Docker, Docker Compose
Orchestration: K3s (Lightweight Kubernetes - planned)
Reverse Proxy: Nginx Proxy Manager
Storage: Local HDD with planned NAS integration
Application Layer
Cloud Services: Nextcloud Hub 25 (Files, Office, Calendar, Contacts, Talk)
Media Server: Jellyfin (streaming), Immich (photos), Audiobookshelf
AI/ML Platform: Ollama (LLM inference), Open WebUI (chat interface)
Home Automation: Home Assistant, Node-RED
Security: UFW, Fail2ban, Let's Encrypt SSL/TLS
DevOps & Monitoring
Infrastructure as Code: Terraform, Ansible
CI/CD: Gitea, Drone CI (planned)
Monitoring: Prometheus, Grafana, Loki
Backup: Automated encrypted backups with 3-2-1 strategy
Security Stack
Network Security: UFW firewall, VLANs, network segmentation
Access Control: 2FA, OAuth2, reverse proxy authentication
Encryption: SSL/TLS, WireGuard VPN, encrypted backups
Monitoring: Wazuh SIEM, ClamAV, fail2ban intrusion prevention
🖥️ Hardware Inventory
Node 1: Primary Server (HP Notebook X7T50UA#ABA)
Component	Specification	Purpose
CPU	Intel 64-bit (UEFI)	Compute, AI inference
RAM	8GB	Service hosting, container runtime
Storage	1TB HDD	Application data, media library
Network	WiFi 802.11ac	Primary connectivity
OS	Ubuntu Server 24.04 LTS	Base platform
Status	✅ Production	Active services
Power	~25W average	Energy efficient
Cost	$0 (e-waste rescue)	Sustainability focus
Node 2: Management Workstation (Microsoft Surface Book Pro)
Component	Specification	Purpose
Role	Development, administration	Client access, management
OS	Windows 11 (transitioning)	Cross-platform testing
Status	🔄 In use	Active management node
Power Infrastructure: APC Back-UPS ES 650 (Thrift Store Rescue)
Component	Specification	Notes
Model	APC BE650G	E-waste rescue
Capacity	650 VA / 390W	Sufficient for Node1 + router
Outlets	8 total (4 battery+surge, 4 surge-only)	Strategic device protection
Surge Protection	340 Joules	Protects against power spikes
Battery Type	Sealed lead-acid (RBC17)	Maintenance-free
Runtime @ 195W	~12 minutes	Half-load operation
Runtime @ 390W	~3 minutes	Full-load operation
Tested Runtime	25 minutes (lamp test)	Exceeds manufacturer specs!
Recharge Time	~24 hours	Full battery recovery
Output Waveform	Stepped approximation sine wave	Suitable for most equipment
Dimensions	3.5"H × 7.1"W × 11.9"D	Compact desktop form factor
Weight	13.7 lb (6.2 kg)	Portable
Acquisition Cost	$11.99 (thrift store)	92% savings vs. retail ($100-150)
Status	✅ Tested & operational	Battery holds charge
Business Value:

Prevents data corruption during power outages
Enables graceful shutdown of services
Protects against voltage fluctuations
Demonstrates production environment thinking
ROI: $138 saved (market value $150 - cost $12)
Connected Equipment:

Node1 (HP Notebook) - Battery backup outlet
T-Mobile Router - Battery backup outlet
Future: Network switch, external storage
Power Continuity Strategy:

Automated shutdown scripts trigger at 20% battery
Critical services save state before shutdown
UPS monitoring via apcupsd daemon (planned)
Battery replacement strategy documented
Future Expansion
Node 3: Higher RAM for intensive AI workloads (target: 16-32GB)
NAS Device: Centralized storage with RAID redundancy
Network Switch: Gigabit managed switch for VLAN segmentation
Additional UPS: Second unit for redundancy (if found at thrift store)
🚀 Project Milestones
✅ Phase 0: Hardware Preparation (Completed - October 2025)
Objective: Rescue and optimize legacy hardware for server deployment

Achievements:

Reduced system startup time by 50%+
Verified disk and system integrity (chkdsk, sfc /scannow)
Reclaimed ~60GB storage through optimization
Extended hardware lifespan, preventing e-waste
Comprehensive documentation for replication
Technical Details:

Performed full disk surface scan and bad sector mapping
System file integrity verification and repair
Registry optimization and startup service audit
Thermal management assessment
BIOS configuration for server workload
Impact: Demonstrated hardware assessment and optimization skills critical for infrastructure planning.

✅ Phase 1: Ubuntu Server Deployment (Completed - October 2025)
Objective: Install and configure production-ready Linux server environment

Achievements:

Clean Ubuntu Server 24.04 LTS installation (no GUI overhead)
Secure WiFi configuration with encrypted credential management
Static IP assignment for service stability
SSH server hardening (key-based auth, fail2ban)
System update automation configured
Technical Implementations:

Netplan YAML configuration with networkd renderer
Secure credential storage (chmod 600 permissions)
UFW firewall baseline rules
Automatic security updates enabled
Time synchronization (chrony)
Security Considerations:

Disabled root login
Password complexity enforcement
Audit logging enabled
Minimal attack surface (no unnecessary services)
Impact: Showcases Linux system administration, security hardening, and infrastructure-as-code principles.

🔄 Phase 2: Private Cloud Foundation (In Progress - October 2025)
Objective: Deploy self-hosted cloud services replacing Google Workspace

Target Services:

 Apache web server deployment
 MariaDB database installation and hardening
 PHP 8.3 configuration for web applications
 Nextcloud Hub 25 - Files, Office, Calendar, Contacts, Talk
 SSL/TLS certificates (Let's Encrypt)
 Dynamic DNS configuration (DuckDNS)
 WireGuard VPN for secure remote access
 Automated backup system (3-2-1 strategy)
Technical Stack:

LAMP architecture (Linux, Apache, MariaDB, PHP)
Nextcloud Office (Collabora Online backend)
CalDAV/CardDAV synchronization protocols
End-to-end encryption for sensitive data
Redis caching for performance optimization
Expected Outcomes:

100% Google Workspace feature parity
Zero monthly SaaS costs (save $288+/year)
Full data sovereignty and privacy
Real-time collaboration capabilities
Cross-platform sync (desktop + mobile)
Business Skills Demonstrated:

Web application deployment
Database administration
Security certificate management
Multi-user system administration
High-availability service design
📋 Phase 3: Media Streaming Platform (Planned - November 2025)
Objective: Self-hosted media server replacing commercial streaming services

Planned Services:

Jellyfin - Movies, TV, music streaming (Netflix/Spotify replacement)
Immich - Photo management with AI face recognition (Google Photos replacement)
Audiobookshelf - Audiobook and podcast management
Calibre-Web - E-book library server
Technical Requirements:

Hardware transcoding configuration
Roku TV integration
Mobile app deployment (iOS/Android)
Media library organization automation
Bandwidth management and QoS
Cost Savings: $30-50/month in streaming subscriptions

📋 Phase 4: AI Infrastructure (Planned - December 2025)
Objective: Private AI/ML platform for local LLM inference

Planned Implementations:

Ollama - Local LLM server (Llama 3, Mistral, others)
Open WebUI - Web-based chat interface with RAG capabilities
Model optimization - Quantization, caching, inference tuning
Multi-user support - Family access to private AI
AI Engineering Skills:

Model deployment and serving
Inference optimization techniques
Resource management for AI workloads
Privacy-preserving AI implementation
Prompt engineering and RAG systems
Unique Value: On-premise AI without cloud API dependencies or data privacy concerns

📋 Phase 5: Home Automation & IoT (Planned - Q1 2026)
Objective: Smart home control and sensor integration

Planned Services:

Home Assistant - Smart home orchestration
Node-RED - Visual automation programming
InfluxDB + Grafana - Time-series data and dashboards
IoT device integration - Heart rate monitors, environmental sensors
IoT Skills Demonstrated:

Real-time data pipeline architecture
Time-series database management
Dashboard creation and visualization
Device protocol integration (MQTT, Zigbee, Z-Wave)
📋 Phase 6: DevOps Automation (Planned - Q1 2026)
Objective: Enterprise-grade infrastructure automation

Planned Implementations:

Terraform - Infrastructure as Code for reproducible deployments
Ansible - Configuration management and automation
Gitea - Self-hosted Git repository
Drone CI - Continuous integration and deployment
Docker Compose - Multi-container orchestration
K3s - Lightweight Kubernetes (if resources permit)
DevOps Portfolio Highlights:

Full GitOps workflow
Automated testing and deployment
Infrastructure versioning and rollback
Secret management (HashiCorp Vault)
Blue-green deployment strategies
📋 Phase 7: Security & Compliance (Planned - Q2 2026)
Objective: Production-grade security posture and monitoring

Security Implementations:

Wazuh - SIEM and intrusion detection
ClamAV - Malware scanning
OSSEC - File integrity monitoring
Zero Trust Network Architecture
Penetration testing and vulnerability assessment
Security documentation and incident response procedures
Compliance & Best Practices:

Security audit logging
Access control policies (RBAC)
Data retention and backup policies
Disaster recovery testing
Security awareness documentation
📊 Key Metrics & Results
Environmental Impact
Metric	Value	Impact
Hardware Rescued	2 devices	Prevented landfill waste
CO₂ Avoided	TBD (measuring)	vs. new hardware manufacturing
Power Consumption	~25W average	Energy-efficient operation
E-Waste Reduction	100% recycled	Zero new hardware purchases
Cost Savings (Projected Annual)
Service Replaced	Monthly Cost	Annual Savings
Google Workspace (2 users)	$24	$288
Google Drive (2TB)	$10	$120
Netflix	$15	$180
Spotify (2 accounts)	$20	$240
VPN Service	$5	$60
Cloud AI APIs	$30	$360
Total Savings	$104/mo	$1,248/year
Technical Performance (Target SLAs)
Uptime: 99.9% availability
Response Time: < 200ms for web services
Backup RPO: < 24 hours
Recovery RTO: < 4 hours
Security Incidents: Zero breaches
🛠️ Getting Started
Prerequisites
Recycled/refurbished x86_64 hardware (4GB+ RAM recommended)
Ubuntu Server 24.04 LTS installation media
Internet connectivity
Basic Linux command line knowledge
Quick Start Guide
bash
# Clone the repository
git clone https://github.com/talljohn-dev/green-AI-lab.git
cd green-AI-lab

# Review documentation
cat docs/00-project-overview.md

# Follow phase-specific guides
ls docs/
Documentation Structure
docs/
├── 00-project-overview.md
├── 01-hardware-preparation.md
├── 02-ubuntu-installation.md
├── 03-network-configuration.md
├── 04-nextcloud-deployment.md
├── 05-security-hardening.md
├── 06-backup-strategy.md
└── architecture/
    ├── network-diagram.png
    ├── service-architecture.png
    └── security-model.png
📚 Documentation
Technical Guides
Hardware Preparation - E-waste assessment and optimization
Ubuntu Server Setup - Installation and base configuration
Network Configuration - WiFi, static IP, security
Nextcloud Deployment - Cloud services installation
Security Hardening - Firewall, SSL, access control
Backup & Recovery - Data protection procedures
Architecture Documentation
Network Topology - Visual diagram of infrastructure
Service Dependencies - Relationship mapping
Security Model - Zero-trust architecture design
Data Flow Diagrams - Information security analysis
Project Resources
Optimization Log - Detailed hardware preparation steps
Results Summary - Machine-readable project metrics
Screenshots - Visual documentation of key milestones
🎯 Skills Demonstrated
This project showcases professional competency in:

Cloud & Infrastructure
✅ Linux system administration (Ubuntu Server)
✅ Web server deployment (Apache, Nginx)
✅ Database administration (MariaDB)
✅ Network architecture and security
✅ SSL/TLS certificate management
🔄 Container orchestration (Docker, K3s)
🔄 Infrastructure as Code (Terraform, Ansible)
DevOps & Automation
✅ Configuration management
✅ Service deployment automation
🔄 CI/CD pipeline implementation
🔄 Monitoring and observability
🔄 GitOps workflows
AI & Machine Learning
🔄 LLM deployment and inference
🔄 Model optimization techniques
🔄 AI infrastructure management
🔄 Privacy-preserving AI implementation
Security Engineering
✅ System hardening
✅ Access control implementation
✅ Encryption and key management
🔄 SIEM and intrusion detection
🔄 Security audit and compliance
Soft Skills
✅ Technical documentation
✅ Project planning and execution
✅ Problem-solving and troubleshooting
✅ Sustainability and cost optimization
✅ Knowledge sharing (open source contribution)
Legend: ✅ Completed | 🔄 In Progress | 📋 Planned

🌱 Sustainability Commitment
Environmental Principles
E-Waste Reduction - Rescue and repurpose discarded hardware
Energy Efficiency - Optimize for low power consumption
Longevity Focus - Extend hardware lifespan through maintenance
Open Source - Zero licensing costs, community-driven development
Documentation - Share knowledge for others to replicate
Carbon Impact
Hardware Lifecycle Extension: +3-5 years per device
Manufacturing Avoidance: No new production emissions
Power Efficiency: <30W average consumption vs. 150W+ new servers
Transportation Reduction: Local e-waste sourcing
🗺️ Roadmap
2025 Q4
 Phase 0: Hardware optimization
 Phase 1: Ubuntu Server deployment
 Phase 2: Nextcloud cloud services (in progress)
 Phase 3: Media streaming platform
2026 Q1
 Phase 4: AI infrastructure deployment
 Phase 5: Home automation integration
 Phase 6: DevOps automation
2026 Q2
 Phase 7: Security hardening & compliance
 Phase 8: Advanced monitoring & observability
 Comprehensive project documentation
Long-term Goals
Multi-node cluster expansion
Kubernetes deployment
Advanced AI/ML workloads
Community tutorials and guides
Open source contributions to upstream projects
🤝 Contributing
This is a personal learning and portfolio project, but contributions, suggestions, and discussions are welcome!

How to Contribute
Report Issues: Found a bug or have a suggestion? Open an issue
Share Knowledge: Document similar builds or improvements
Collaborate: Interested in e-waste cloud projects? Let's connect
Community
Discussions: GitHub Discussions (coming soon)
Blog: Technical writeups at [your-blog-link]
LinkedIn: Connect for professional networking
📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

Open source software used in this project retains its original licenses.

👤 About
John Vasquez-Tallacksen
Cloud & AI Infrastructure Engineer (Aspiring)
Los Angeles, CA

Building enterprise-grade infrastructure from e-waste while transitioning into cloud architecture and AI infrastructure roles.

Connect
GitHub: @talljohn-dev
LinkedIn: john-vasquez-tallacksen
Email: [your-email]
Blog: [your-blog-link]
Career Goals
Leveraging this hands-on infrastructure project to transition into:

Cloud Architecture roles ($120-180k)
DevOps Engineering positions ($130-180k)
AI Infrastructure Engineer roles ($180-250k+)
This project demonstrates real-world skills employers value:
Self-hosting, security-first design, cost optimization, sustainability, and continuous learning.

🙏 Acknowledgments
Ubuntu Community - For excellent server documentation
Nextcloud Team - For open-source collaboration platform
Homelab Community - For inspiration and knowledge sharing
Open Source Contributors - For making self-hosting possible
📈 Project Stats
Show Image
Show Image
Show Image

Last Updated: October 2025
Project Status: Active Development
Current Phase: 2 of 7

<div align="center">
🌍 Building the Future, One Rescued Laptop at a Time
Green AI Lab - Where sustainability meets innovation

⬆ Back to Top

</div>
