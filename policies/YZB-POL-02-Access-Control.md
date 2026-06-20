# YZB-POL-02: Access Control & Cryptography Policy

**Document Reference:** YZB-POL-02-2026-V1  
**Classification:** Internal Use Only  
**Effective Date:** June 20, 2026  
**Version:** 1.0  
**Owner:** Product Lead / GRC Compliance Lead  

---

## 1. Purpose
This policy defines the structural standards for managing identity authentication, user privileges, and cryptographic keys to shield Yearzbuddy data from account takeovers, insider threats, and intellectual property leaks in compliance with **ISO/IEC 27001:2022 Controls A.5.15, A.5.17, and A.8.24**.

## 2. Scope
This policy applies to all administrative system access points, developer environments, cloud infrastructure backends (AWS/GCP), and artist/label account dashboards managing content distribution under Yearzbuddy.

## 3. Access Control Framework (Control A.5.15)
1. **Principle of Least Privilege (PoLP):** Access to Yearzbuddy systems is restricted by default. Users are granted the minimum level of access required to complete their explicit operational tasks.
2. **Role-Based Access Control (RBAC):** Privileges are mapped directly to defined business roles:
   * **Director / Executive:** Read-only access to master data pools; full authorization over company corporate assets and royalty payouts.
   * **Product / Engineering Lead:** Full administrative control over code deployment environments, infrastructure configuration, and API nodes. No access to raw artist royalty account vectors.
   * **A&R / Business Manager:** Read/Write permissions for artist onboarding, metadata modification, and ingestion queue validations. Zero download permissions for unreleased master audio.
3. **Account Review Cadence:** User privileges and system access rights must be audited and flushed quarterly to eliminate credential accumulation.

## 4. Multi-Factor Authentication & Identity Protection (Control A.5.17)
1. **Mandatory MFA:** Multi-Factor Authentication (MFA) must be enforced across 100% of internal employee accounts, virtual contractor tools, and developer code repositories.
2. **Acceptable MFA Factors:** Permissible authentication tracking methods include secure Authenticator applications (Time-Based One-Time Password - TOTP) or hardware cryptographic security keys. Static password authentication alone is strictly prohibited.
3. **Session Termination:** Administrative system panels must auto-terminate active user sessions following 15 minutes of inactivity to defend endpoints in untrusted physical environments.

---

## 5. Cryptographic Architecture & Key Management (Control A.5.34 & A.8.24)
To maintain complete integrity over Yearzbuddy's digital distribution loop, strict encryption baselines are codified into the architecture:

### 5.1 Data Encryption Standards
* **Data In-Transit:** All ingestion payloads and communication packets sent across artist panels must navigate through secure TLS 1.3 encryption channels. Delivery to global Digital Streaming Platforms (DSPs) must occur via verified, encrypted DDEX XML distribution targets.
* **Data At-Rest:** High-value Tier 1 information assets—explicitly unreleased master tracks (`.wav`/`.flac`) and financial routing databases—must be stored in cloud repositories using **AES-256 block encryption**.

### 5.2 Cryptographic Key Management Lifecycle
1. **Isolated Vault Storage:** All system symmetric/asymmetric cryptographic keys, SSL certificates, and third-party API interface tokens must reside within a centralized, hardware-backed cloud key management vault (e.g., AWS KMS).
2. **Key Rotation Schedules:** Data protection master keys must rotate automatically every 90 calendar days to restrict vulnerability exposure timeframes.
3. **Key Revocation:** In the event of a suspected cloud configuration gap or employee offboarding, the respective administrative security key must be immediately revoked, destroyed, and regenerated according to incident mitigation playbooks.
