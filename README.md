# 🔐 Microsoft Active Directory Certificate Services (AD CS)

**GBA 5200 | Adam Gomez**

This project explores Microsoft’s Active Directory Certificate Services (AD CS) and its real-world use in securing enterprise communication through Public Key Infrastructure (PKI). The walkthrough includes deploying a domain environment, creating users, and issuing certificates to enforce authentication, confidentiality, and encryption within an organization.

---

## 🎥 Video Demonstration

**YouTube**: [AD CS Lab Demo – Creating a Domain, Users, and Certificates](https://youtu.be/YOUR-LINK-HERE)

---

## 🖥️ Lab Environment

- **Windows Server** (as Domain Controller)
- **Active Directory Certificate Services (AD CS)**
- **Microsoft Management Console (MMC)**
- **Virtualized Lab** (e.g., Hyper-V / Azure / VMware)

---

## 🧩 Key Technologies and Concepts

- Public Key Infrastructure (PKI)
- Enterprise CA vs Standalone CA
- Certificate Hierarchy (Root, Issuing, Intermediate)
- Windows Certificate Store
- Role-Based & Attribute-Based Access Control
- Digital Signatures and SSL/TLS

---

## 🛠️ Walkthrough: Project Steps

### 🔹 Step 1: Create a Windows Domain

- Deployed a Windows Server virtual machine
- Promoted it to a Domain Controller (`example.local`)

### 🔹 Step 2: Add Users and Groups

- Created user accounts in Active Directory
- Assigned to department-based groups (e.g., IT, Marketing)

### 🔹 Step 3: Install AD CS

- Installed the **AD CS Role** via Server Manager
- Chose **Enterprise Root CA** configuration
- Set hash algorithm to **SHA-256**
- Chose key length, validity period, and storage paths

### 🔹 Step 4: Issue Certificates

- Created certificate templates
- Issued **User Certificates** via MMC
- Auto-enrolled **Computer Certificates** through Group Policy
- Validated issuance through Certificate Store

---

## 🔐 Use Cases

### 📧 Secure Email (S/MIME)

- Digitally signs and encrypts emails to ensure sender authenticity and message privacy

### 🌐 Secure Wireless Networks (802.1X)

- Requires valid device certificates to access enterprise Wi-Fi

### 🛡️ Virtual Private Networks (VPN)

- Enforces certificate-based authentication for secure remote access

### 🌍 Web Server Certificates (SSL/TLS)

- Protects data transmission and ensures website legitimacy

---

## 🧾 Certificate Types

| Certificate Type     | Purpose                                                                 |
|----------------------|-------------------------------------------------------------------------|
| **User Certificates** | Authenticate users, encrypt email, enable digital signatures           |
| **Computer Certificates** | Authenticate domain-joined devices, secure communications         |
| **Web Server Certificates** | Encrypt web traffic using HTTPS via SSL/TLS                     |

---

## 🛡️ PKI Hierarchy & Security

- **Root CA**: Central trust anchor
- **Two-Tier Hierarchy**: Best practice with isolated offline Root CA and online Issuing CA
- **Intermediate CAs** (optional): Add policy-based segmentation and security boundaries

---

## ⚖️ Advantages of AD CS

- ✅ Full control over certificate lifecycle and trust model
- ✅ Integrated with Active Directory
- ✅ Enables automation via Group Policy and auto-enrollment
- ✅ Supports strong cryptography (SHA-256+)
- ✅ Helps enforce Zero Trust security principles

