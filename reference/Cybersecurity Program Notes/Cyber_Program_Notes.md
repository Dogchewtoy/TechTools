# This page is a collection of recommended practices, my own "best" practices, concerns, and ideas #

**Recommended Policies**

* Acceptable Use Policy
* BYOD Policy
* Patching Policy
* Incident Management Policy
* Supporting Policies from the applicable RM Framework (media handling, physical security, supply chain, etc.)

**Categories and Areas of Opportunity**

* Access Control
    * Good password policies - with an eye towards modern authentication (no/long password exp, MFA with geolocation, PIN/biometric, and perhaps physical Yubi-style key for admins)
    * Multifactor auth with soft token on user devices, making sure the MFA request and confirmation come from the same network or are geographically close
    * Corporate-owned device registration (Intune or similar and device TPM)
    * Guests segmented onto different network
    * Ideally, enterprise NAC for corporate networks with device certificates
    * Separate authentication for non-PKI/802.1x devices
    * Least Privilege
    * Role-based access control and discretionary access control
        * Assigned to groups vs individual users where possible
    * Privileged Account reviews
    * Account Provisioning Workflow - automate where possible, automatic account disable
    * Remote Access: MFA is a must, with firewall boundary and policy control
    * Zero Trust Additions: continuous authentication, conditional access, PAM, PIM, Federated SSO, user behavior analysis

* Separation of Duties

* Cyber security training/awareness program

* Configuration Management
    * Backup appliance configurations
    * Change detection
    * Device hardening standards

* Inventory Management
    * Supply Chain Management
    * CMDB
    * MDM/Device Management
    * Application Inventory
    * 3rd Party Software Inventory

* Change Management Process
    * Change Mgmt Board
    * Change Mgmt Process
    * Change Mgmt Categories

* Risk Management Process
    * Asset Inventory with values
    * Risk Inventory
    * Security Impact Analyses
    * Risk Mitigations
    * Risk Acceptance (Documented)

* Incident Response
    * Pre-Incident 
        * Planning, Testing, Gaming
        * Categorization
        * Communication Plan
    * Detection
    * Identification, Analysis, and Scoping
    * Response
    * Escalation
    * Recovery
    * Post-mortem

* Backups
    * Type
    * Retention
    * Replication
    * Verify encryption keys are backed up

* Contingency Planning
    * Planning, Scoping, SLA definition
    * COOP
    * DR
    * BCP

* Media Control
    * Internal
    * External
    * Removable
    * Sharing
    * Spills
    * Decommission/Destruction

* Patch Management
    * Feeds
    * Testing
    * Rollback
    * UAT

* Monitoring
    * Infrastructure Monitoring, Alerting
    * NOC
    * SOC, SIEM
    * Log collection

* Auditing
    * Scope
    * Frameworks
    * Schedule
    * Map where you stand vs where you need to be

**Security Architecture**

* Endpoint
    * Device: AV, EDR, XDR, HIPS, disk encryption, MDM, device location
    * Account: MFA, Conditional Access, UBA, Least Privilege, PIM/PAM
* Network Access: 802.1x, NAC, client isolation
* Network Transport: Secure Routing, VLAN assignment, VLAN trunking
* Network Segmentation: Macro to micro
* Network Boundary Services: ACL, IDS/IPS
* Network Services: DNS Security
* Network Edge: WAF, Reverse Proxy, DMZ, micro-segmentation
* Vulnerability Management
    * Internal and external priv/non-priv vulnerability scans
    * Regular pen tests (include automated)
    * Consider agents for critical resources
* Application Development Security
    * SAST in dev pipeline
    * SCA
    * DAST and IAST where possible
    * Penetration Testing
    * Scan repos for credentials and strings
    * Managed IDs for cloud apps
    * Standards: AppDev STIG, OWASP
* Microsoft Directory Security
    * ADDS
        * Kerberos
            * Pass the hash
            * kerberoasting
            * SPNs
            * GPO
            * Limit Domain Admins
        * Disable NTLM
    * Entra ID/Azure
        * Primary Refresh Token (PRT)
        * Token Stealing
        * Graph api abuse
* VMWare Security
    * Play vulnerability (AD Group)








