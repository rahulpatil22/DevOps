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




## 🧭 Summary Table (Quick Revision)

| Protocol        | Port        | Usage                 |
|-----------------|-------------|------------------------|
| HTTP            | 80          | Websites               |
| HTTPS           | 443         | Secure websites/APIs   |
| SSH             | 22          | Remote server access   |
| DNS             | 53          | Domain resolution      |
| FTP             | 21          | File transfers         |
| SMTP            | 25 / 587    | Sending alerts         |
| MySQL           | 3306        | Database               |
| PostgreSQL      | 5432        | Database               |
| Redis           | 6379        | Caching                |
| MongoDB         | 27017       | NoSQL DB               |
| Kubernetes API  | 6443        | Cluster control        |
| Docker Daemon   | 2375 / 2376 | Container builds       |

3. AWS EC2 and Security Groups
Launch an AWS EC2 instance (free tier is fine).
Learn about Security Groups, their rules, and their significance in securing cloud instances.
Task: Write a step-by-step guide or blog on how to create and configure Security Groups.

📌 Table of Contents

📘 Overview

🧭 Quick Concepts

🛠 Prerequisites

✅ Step 1 — Launch an EC2 Instance

✅ Step 2 — Create & Configure Security Groups

🌐 Inbound & Outbound Rule Examples

💻 AWS CLI Commands

🧱 Terraform Example

🔐 Best Practices

🧪 Troubleshooting

📎 Quick Port Reference

📌 Recap

📘 Overview

EC2 (Elastic Compute Cloud)
A virtual machine (server) you can launch in AWS.

Security Group (SG)
A stateful virtual firewall attached to EC2 instances that controls:

Inbound traffic → What can enter the EC2 instance

Outbound traffic → What EC2 can access outside

Only ALLOW rules (No deny rules)

Automatically allows return traffic (stateful)

🧭 Quick Concepts
Concept	Meaning
Inbound rules	Traffic allowed toward EC2
Outbound rules	Traffic allowed from EC2
CIDR	IP range (e.g., 0.0.0.0/0, 203.0.113.10/32)
/32	Single IP address
Stateful	Response traffic automatically allowed
Least privilege	Only open required ports
🛠 Prerequisites

AWS account

IAM user with EC2 permissions

SSH key pair (for Linux access)

(Optional) AWS CLI installed

(Optional) Terraform installed

✅ Step 1 — Launch an EC2 Instance

Go to AWS Console → EC2 → Instances → Launch Instances

Select Amazon Linux 2 AMI (Free-tier eligible)

Instance type: t2.micro

Create/download key pair:

my-keypair.pem
chmod 400 my-keypair.pem


Network settings → Create new Security Group (or use default)

Launch the instance

Connect via SSH:

ssh -i my-keypair.pem ec2-user@<PUBLIC_IP>

✅ Step 2 — Create & Configure Security Groups
🎯 Create a Security Group

Go to EC2 → Security Groups → Create Security Group

Name:

sg-dev-ssh-http


Description:

Allow SSH from my IP and HTTP from anywhere


Choose correct VPC

🎯 Add Inbound Rules (Examples)
Type	Port	Source	Purpose
SSH	22	YOUR_IP/32	Secure login
HTTP	80	0.0.0.0/0	Web traffic
HTTPS	443	0.0.0.0/0	Secure web traffic
MySQL	3306	10.0.1.0/24	App → DB
🎯 Outbound Rules

Default:

ALL traffic → 0.0.0.0/0


Recommended for most cases unless tightened security is required.

🎯 Attach Security Group to EC2

Go to EC2 → Instances → Select instance

Actions → Security → Change security groups

Add the newly created SG

Save

🌐 Inbound & Outbound Rule Examples (Real Use Cases)
Use Case	Inbound Rule	Outbound Rule
SSH access	22 from YOUR_IP/32	Allow all
Public Web Server	80/443 from 0.0.0.0/0	Allow all
Private Database	3306 from App SG	Allow all
Redis Cache	6379 from App SG	Allow all
💻 AWS CLI Commands
Create Security Group
aws ec2 create-security-group \
  --group-name sg-dev-ssh-http \
  --description "Allow SSH and HTTP" \
  --vpc-id vpc-1234567890abcdef

Add SSH Rule
aws ec2 authorize-security-group-ingress \
  --group-id sg-1234567890abcdef \
  --protocol tcp --port 22 \
  --cidr 203.0.113.10/32

Add HTTP Rule
aws ec2 authorize-security-group-ingress \
  --group-id sg-1234567890abcdef \
  --protocol tcp --port 80 \
  --cidr 0.0.0.0/0

Attach SG to EC2
aws ec2 modify-instance-attribute \
  --instance-id i-1234567890abcdef \
  --groups sg-1234567890abcdef

🧱 Terraform Example
provider "aws" {
  region = "us-east-1"
}

resource "aws_security_group" "web" {
  name        = "sg-web-ssh"
  description = "Allow SSH & HTTP"

  ingress {
    from_port   = 22
    to_port     = 22
    protocol    = "tcp"
    cidr_blocks = ["203.0.113.10/32"]
  }

  ingress {
    from_port   = 80
    to_port     = 80
    protocol    = "tcp"
    cidr_blocks = ["0.0.0.0/0"]
  }

  egress {
    from_port   = 0
    to_port     = 0
    protocol    = "-1"
    cidr_blocks = ["0.0.0.0/0"]
  }
}

resource "aws_instance" "web" {
  ami                    = "ami-0abcdef1234567890"
  instance_type          = "t2.micro"
  key_name               = "my-keypair"
  vpc_security_group_ids = [aws_security_group.web.id]
}


Deploy:

terraform init
terraform apply -auto-approve

🔐 Best Practices

Allow SSH only from specific IPs, not 0.0.0.0/0

Use Security Group references (SG-to-SG communication)

Place DBs in private subnets

Use HTTPS everywhere

Tag resources (Environment, Owner, Purpose)

Use Terraform for production environments

Enable VPC Flow Logs to monitor traffic



