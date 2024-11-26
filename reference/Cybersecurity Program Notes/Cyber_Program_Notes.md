# This page is a collection of recommended practices, my own "best" practices, concerns, and ideas #

**Recommended Policies**

* Acceptable Use Policy
* BYOD Policy
* Patching Policy
* Incident Management Policy
* Supporting Policies from the applicable RM Framework (media handling, physical security, supply chain, etc.)


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




