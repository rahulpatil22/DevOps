#️⃣ 1. OSI & TCP/IP Models – With Real-World Examples
🖼 OSI Model (7 Layers)
<img width="5667" height="2834" alt="image" src="https://github.com/user-attachments/assets/53c94ef9-1f1b-48ef-a89f-87ebdf524201" />
1️⃣ Application Layer (Layer 7)

Purpose: Services for apps (browser, email, etc.)

Examples:

HTTP/HTTPS → Websites

SMTP → Sending emails

DNS → Domain name resolution

FTP/SFTP → File transfer

2️⃣ Presentation Layer (Layer 6)

Purpose: Data formatting & encryption.

Examples:

TLS/SSL → HTTPS security

JPEG/PNG → Image encoding

MP3/MP4 → Media encoding

JSON/XML → API formatting

3️⃣ Session Layer (Layer 5)

Purpose: Manage sessions/connection lifecycle.

Examples:

Login sessions

API tokens

RDP sessions

Large file uploads

4️⃣ Transport Layer (Layer 4)

Purpose: Reliable or fast delivery.

✔ TCP (Reliable)

Web browsing

Email

File transfer

✔ UDP (Fast)

YouTube streaming

Online gaming

VoIP calls

5️⃣ Network Layer (Layer 3)

Purpose: Routing & IP addressing.

Examples:

IPv4/IPv6

Routers

Traceroute

VPN

6️⃣ Data Link Layer (Layer 2)

Purpose: MAC addressing & frames.

Examples:

Switches

ARP

WiFi frames

Ethernet

7️⃣ Physical Layer (Layer 1)

Purpose: Transmission of bits.

Examples:

Fiber cables

Ethernet cables

WiFi radio signals

NIC cards

🌐 TCP/IP Model (4 Layers)
<img width="726" height="601" alt="image" src="https://github.com/user-attachments/assets/1958279f-db4e-4528-80c4-6f238634cf91" />
1️⃣ Application Layer

(OSI Layers 5, 6, 7 combined)

Examples:

HTTP/HTTPS

DNS

SMTP

DHCP

SSH

2️⃣ Transport Layer

Examples:

TCP

UDP

3️⃣ Internet Layer

(OSI Network layer)

Examples:

IP

ICMP (ping)

NAT

Routing

4️⃣ Network Access Layer

(OSI Layers 1 & 2 combined)

Examples:

Ethernet

WiFi

ARP

#️⃣ 2. Protocols & Ports Every DevOps Engineer Must Know
<img width="1444" height="1882" alt="image" src="https://github.com/user-attachments/assets/d2304573-9e14-4137-8dd3-090ce87dd283" />
🚀 1. Web Protocols
HTTP – Port 80

Used for:

Health checks

Microservice communication

Load balancing (NGINX/Apache)

CI/CD test stages

HTTPS – Port 443

Used for:

Secure APIs

Kubernetes Ingress

Cloud dashboards

GitHub / DockerHub

🔐 2. Remote Access & Config Management
SSH – Port 22

Used for:

EC2/VM login

Jenkins deployments

Git SSH

Ansible

SCP/SFTP

SFTP – Port 22

Used for secure file transfers.

📦 3. File Transfer Protocols
FTP – Port 21

Used in legacy systems.

FTPS – Port 990 / 989

Secure FTP over TLS.

🌍 4. DNS & Name Resolution
DNS – Port 53 (TCP/UDP)

Used for:

Kubernetes service discovery

Cloud DNS

Microservice names

Example:

frontend-service.default.svc.cluster.local

✉ 5. Email Protocols (Alerts & Monitoring)
Protocol	Port	Use in DevOps
SMTP	25 / 587	Send alert emails
IMAP	143 / 993	Read emails
POP3	110 / 995	Legacy retrieval
🗂 6. Application & API Protocols
REST APIs (HTTP/HTTPS)

Used in:

Kubernetes API

Terraform providers

GitHub Actions

Cloud APIs

gRPC – Port 50051

Used for high-speed microservices.

⚡ 7. Database Ports
Database	Port	Use
MySQL	3306	App DB
PostgreSQL	5432	Cloud apps
MongoDB	27017	NoSQL
Redis	6379	Cache
🧱 8. Container & Orchestration Ports
Docker Daemon – 2375/2376

Used for:

Remote builds

Swarm

Kubernetes Components
Component	Port	Purpose
API Server	6443	Cluster control
kubelet	10250	Node communication
ETCD	2379–2380	Cluster state
NodePort	30000–32767	App exposure
🌐 9. VPN & Security
HTTPS/TLS

Secures all DevOps traffic.

OpenVPN – Port 1194
IPSec – Ports 500 / 4500


🧭 Summary Table (Quick Revision)
Protocol	Port	Usage
HTTP	80	Websites
HTTPS	443	Secure websites
SSH	22	Remote access
DNS	53	DNS resolution
FTP	21	File transfer
SMTP	25/587	Alerts
MySQL	3306	Database
PostgreSQL	5432	Database
Redis	6379	Cache
MongoDB	27017	NoSQL
K8s API	6443	Cluster
Docker Daemon	2375/2376	Docker engine
