# Multi-Cloud Deployment: AWS to Azure VPN Architecture

## 🧠 Project Summary
This project establishes a secure, cost-effective, and scalable VPN tunnel between AWS and Azure. It demonstrates a hybrid architecture for cloud migration or multi-cloud redundancy, enabling communication between a VPC in AWS and a VNet in Azure.

---

## 🏗️ Architecture Overview

- **AWS Side**
  - Virtual Private Cloud (VPC)
  - Customer Gateway (CGW)
  - Virtual Private Gateway (VGW)
  - Site-to-Site VPN

- **Azure Side**
  - Virtual Network (VNet)
  - Virtual Network Gateway (VPN)
  - Local Network Gateway (on-premises simulator)
  - Connection

---

## ⚙️ Services Used

| Category       | AWS Services             | Azure Services             |
|----------------|--------------------------|----------------------------|
| Networking     | VPC, VPN Gateway         | VNet, Virtual Network Gateway |
| Security       | Security Groups, NACLs   | NSGs                       |
| Monitoring     | CloudWatch               | Network Watcher, Monitor  |

---

## 💰 Cost Estimate

### AWS VPN Gateway
- $0.05/hour (standard VPN connection)
- Data transfer: $0.09/GB (first 10TB)

### Azure VPN Gateway
- Basic SKU: ~$0.04/hour
- Data transfer: ~$0.035/GB

### 🔢 Daily & Monthly Estimate (Light Use)
| Cloud  | Resource         | Cost/Day | Cost/Month |
|--------|------------------|----------|------------|
| AWS    | VPN Gateway      | $1.20    | ~$36       |
| Azure  | VPN Gateway      | $0.96    | ~$29       |
| **Total** | —              | **$2.16** | **~$65**   |

---

## 🔐 Security Best Practices
- Limit inbound/outbound access using NACLs and NSGs
- Use BGP if possible for routing
- Monitor connection with CloudWatch (AWS) and Network Watcher (Azure)

---

## 📁 Folder Structure
```
/multicloud_deployment_repo/
│
├── README.md
├── diagrams/
│   └── architecture.png
└── docs/
    └── multicloud_deployment_writeup.docx
```

---

## 🔧 Future Enhancements
- Automate setup using Terraform
- Add cross-cloud monitoring alerts
- Integrate traffic logs into centralized SIEM
