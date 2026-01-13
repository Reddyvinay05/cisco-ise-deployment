# Cisco ISE Deployment Project

## Overview
This project documents an enterprise-scale Cisco Identity Services Engine (ISE) deployment for secure network access control, device profiling, and network segmentation. The solution provides centralized authentication, authorization, and accounting (AAA) services across wired and wireless infrastructure.

## Project Scope

### Business Requirements
- Implement secure 802.1X authentication for corporate devices
- Deploy guest wireless access with self-service portal
- Enable automated device profiling and network segmentation
- Enforce role-based access control policies
- Provide visibility into all network endpoints

### Technical Objectives
- Deploy ISE in distributed architecture (Primary + Secondary PAN/MNT nodes)
- Integrate with Active Directory for user authentication
- Configure wired and wireless 802.1X with EAP-TLS and PEAP
- Implement MAC Authentication Bypass (MAB) for IoT devices
- Set up guest portal with sponsor approval workflow
- Deploy TrustSec for security group-based segmentation

## Architecture

### ISE Deployment Model
- **Primary Policy Administration Node (PAN)**: Configuration and policy management
- **Secondary PAN**: High availability and failover
- **Monitoring & Troubleshooting (MNT) Nodes**: Logging and reporting (2x nodes)
- **Policy Service Nodes (PSN)**: RADIUS authentication (4x distributed PSNs)

### Network Integration
- **Wireless Controllers**: Cisco 9800 WLC (3x)
- **Access Switches**: Cisco Catalyst 9300 series with 802.1X
- **Distribution/Core**: Cisco Nexus 9000 series
- **Active Directory**: Integration for user/computer authentication

## Key Features Implemented

### 1. 802.1X Authentication
- **EAP-TLS**: Certificate-based authentication for corporate devices
- **PEAP-MSCHAPv2**: Username/password authentication for BYOD
- **EAP-FAST**: Secure tunnel for legacy devices
- Dynamic VLAN assignment based on user/device identity

### 2. MAC Authentication Bypass (MAB)
- Automatic profiling for printers, IP phones, cameras, IoT devices
- Custom profiling policies for OT/IoT endpoints
- Authorization profiles with specific VLAN and ACL assignments

### 3. Guest Access
- Self-service guest portal with SMS/email verification
- Sponsor approval workflow for contractor access
- Time-based access control (auto-expiration)
- Guest VLAN isolation and bandwidth throttling

### 4. Device Profiling
- Automated endpoint classification using:
  - DHCP
  - HTTP User-Agent
  - MAC OUI
  - SNMP
  - NetFlow
- Custom profiling rules for specialized devices

### 5. TrustSec Security Group Tagging
- Security Group ACLs (SGACLs) for micro-segmentation
- Dynamic security group assignment based on user/device context
- Integration with Cisco firewalls and switches

### 6. Compliance and Posture Assessment
- Endpoint compliance checks (antivirus, OS patches, disk encryption)
- AnyConnect NAC module for posture validation
- Quarantine VLAN for non-compliant devices

## Authentication Flow

```
[Endpoint] --> [802.1X Supplicant] --> [Authenticator: Switch/WLC] --> [RADIUS] --> [ISE PSN]
     |
     v
[ISE Policy Engine]
     |
     +--> [Active Directory Lookup]
     +--> [Device Profiling]
     +--> [Authorization Policy Evaluation]
     |
     v
[RADIUS Access-Accept with Attributes]
     |
     +--> VLAN Assignment
     +--> ACL/dACL
     +--> Security Group Tag (SGT)
```

## Technologies Used

- **Cisco ISE 3.2**: Identity and access control platform
- **802.1X (EAP-TLS, PEAP, EAP-FAST)**: Network access authentication
- **RADIUS**: Authentication protocol
- **Active Directory**: User/computer identity source
- **Cisco TrustSec**: Security group-based segmentation
- **Cisco 9800 WLC**: Wireless LAN controllers
- **Cisco Catalyst 9300**: Access layer switches with 802.1X
- **AnyConnect NAC**: Endpoint posture assessment
- **pxGrid**: Platform exchange for security ecosystem integration

## Configuration Highlights

### Policy Sets
1. **Wired 802.1X Policy**: EAP-TLS for corporate laptops/desktops
2. **Wireless 802.1X Policy**: PEAP for BYOD and corporate wireless
3. **MAB Policy**: Profiling-based authorization for IoT/OT devices
4. **Guest Policy**: CWA (Central Web Authentication) with portal redirect

### Authorization Profiles
- **Corporate_Wired**: VLAN 10, full network access
- **Corporate_Wireless**: VLAN 20, internet + internal resources
- **BYOD**: VLAN 30, restricted access with dACL
- **Guest**: VLAN 50, internet-only, rate-limited
- **IoT_Devices**: VLAN 60, isolated with specific ACLs
- **Quarantine**: VLAN 99, remediation portal access only

## Challenges & Solutions

### Challenge 1: Legacy Device Support
- **Issue**: Older devices without 802.1X supplicant (printers, cameras)
- **Solution**: Implemented MAB with custom profiling policies and dedicated VLANs

### Challenge 2: Certificate Management
- **Issue**: Distributing and managing certificates for EAP-TLS
- **Solution**: Integrated with internal PKI, automated certificate enrollment via SCEP

### Challenge 3: Guest User Experience
- **Issue**: Complex guest onboarding process
- **Solution**: Simplified self-service portal with SMS verification, QR code for Wi-Fi

### Challenge 4: High Availability
- **Issue**: Single point of failure for authentication
- **Solution**: Deployed redundant PAN and multiple PSNs with load balancing

## Results & Outcomes

- ✅ **99.9% uptime** for authentication services
- ✅ **5,000+ endpoints** successfully authenticated daily
- ✅ **Zero trust network** access model implemented
- ✅ **Reduced security incidents** by 60% through device profiling and segmentation
- ✅ **Compliance achieved** with internal security policies and industry standards
- ✅ **Guest access provisioning** reduced from 30 minutes to 2 minutes

## Monitoring & Reporting

- Real-time authentication dashboards in ISE
- Failed authentication alerting and troubleshooting
- Endpoint profiling reports
- RADIUS live logs for debugging
- Integration with Splunk for long-term log analysis

## Future Enhancements

- [ ] Extend TrustSec to data center fabric (ACI integration)
- [ ] Implement ISE PxGrid integration with SIEM
- [ ] Add profiling for additional IoT device types
- [ ] Deploy ISE passive identity services for non-802.1X segments
- [ ] Automate compliance reporting with custom scripts

## Skills Demonstrated

- Enterprise ISE architecture and deployment
- 802.1X protocol expertise (EAP methods, RADIUS)
- Network security policy design
- Active Directory integration
- Device profiling and classification
- Guest access workflows
- TrustSec security group tagging
- High availability design
- Troubleshooting complex authentication issues
- Documentation and knowledge transfer

## Documentation

- Network topology diagrams (in `/diagrams` folder)
- ISE policy configuration exports (in `/configs` folder)
- Deployment runbook and troubleshooting guide (in `/docs` folder)

## Contact

For questions about this project, feel free to reach out via [LinkedIn](https://www.linkedin.com/in/yourprofile) or email.

---

**Note**: All configurations and screenshots in this repository have been sanitized to remove sensitive information.
