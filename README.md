🔐 Microsoft Active Directory Certificate Services (AD CS)
GBA 5200 | Adam Gomez

This project explores Microsoft’s Active Directory Certificate Services (AD CS) and its real-world use in securing enterprise communication through Public Key Infrastructure (PKI). The walkthrough includes deploying a domain environment, creating users, and issuing certificates to enforce authentication, confidentiality, and encryption within an organization.

🎥 Video Demonstration
YouTube: AD CS Lab Demo – Creating a Domain, Users, and Certificates

(Replace the link once your video is uploaded)

🖥️ Lab Environment
Windows Server (AD Domain Controller)

Active Directory Certificate Services Role

Microsoft Management Console (MMC)

Virtualized Lab via Hyper-V / Azure / VMware

🧩 Key Technologies and Concepts Covered
Public Key Infrastructure (PKI)

Enterprise CA vs Standalone CA

Two-Tier Certificate Authority Hierarchy

Symmetric vs Asymmetric Encryption

Windows Certificate Store

Digital Signatures & SSL/TLS

Role- and Attribute-Based Access Control

🛠️ Walkthrough: Project Steps
🔹 Step 1: Create a Windows Domain Environment
Deployed a virtual Windows Server machine

Promoted it to a Domain Controller

Created a new Active Directory domain (example.local)

🔹 Step 2: Add Users and Groups
Created multiple user accounts via Active Directory Users and Computers (ADUC)

Assigned users to different groups based on department (e.g., Marketing, IT, Finance)

🔹 Step 3: Install Active Directory Certificate Services (AD CS)
Installed AD CS Role via Server Manager

Configured the role as an Enterprise Root CA

Selected SHA-256 as the hash algorithm for the CA

Set a certificate validity period and storage location for logs and certificate database

🔹 Step 4: Issue Certificates to Users and Devices
Used Certificate Templates and the MMC to enroll user certificates

Assigned certificates to specific users for S/MIME and secure email

Demonstrated computer certificate auto-enrollment

Used Group Policy to push certificate policies automatically

🔐 Use Cases for AD CS
📧 Secure Email (S/MIME)
Ensures that emails are digitally signed and encrypted

Verifies sender identity and protects message integrity

🌐 Secure Wireless Networks (802.1X)
Validates device access through certificate-based authentication

Encrypts communication between endpoint and access points

🌍 Virtual Private Networks (VPN)
Replaces username/password logins with certificate-based authentication

Creates encrypted tunnels using IPSec

🔒 Web Server Security (SSL/TLS)
Protects login credentials and sensitive data sent via websites

Uses server certificates to encrypt HTTPS sessions

🧾 Types of Certificates Issued
Certificate Type	Purpose
User Certificates	Authenticates users, signs emails, encrypts communications
Computer Certificates	Secures machine identity for domain communication
Web Server Certificates	Encrypts web traffic using SSL/TLS
(Others possible: Smart Cards, Device Auth, RADIUS Auth)	

🛡️ Certificate Hierarchy
Root CA: Single point of trust (configured as Enterprise CA)

Two-Tier Model: Suggested for larger orgs (root + issuing CAs)

Offline Root Best Practice: Added security by isolating the trust anchor

⚖️ Advantages of AD CS
✅ Full control over certificate lifecycle
✅ Integrated with Active Directory
✅ Supports modern cryptography (SHA-256+)
✅ Enables Zero Trust policies with strict access controls
✅ Certificate auto-enrollment and GPO integration
