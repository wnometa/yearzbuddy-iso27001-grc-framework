# YZB-POL-04: Supplier & Third-Party Security Policy

**Document Reference:** YZB-POL-04-2026-V1  
**Classification:** Internal Use Only  
**Effective Date:** June 20, 2026  
**Version:** 1.0  
**Owner:** Director / Product Lead  

---

## 1. What This Policy Is About
Yearzbuddy relies on trusted external partners to build and host our infrastructure. This includes the external software development agency building our platform and cloud infrastructure providers like AWS or GCP. 

While we offload physical server hosting to these third parties, we cannot offload our security responsibility. This policy maps out the simple rules we use to vet our partners, hold them accountable, and protect our data pipelines from supply-chain threats under **ISO/IEC 27001:2022 (Controls A.5.19 - A.5.23)**.

## 2. Rules for Core Partners & Vendors

### 2.1 The External Development Agency (Control A.5.19 & A.5.20)
Before the external dev company writes code or configures modules for our ecosystem, they must agree to our security baselines:
* **Background Check Safeguards:** The agency must ensure that any engineer assigned to Yearzbuddy's codebase has been vetted and has signed a binding Non-Disclosure Agreement (NDA).
* **Secure Code Delivery:** Code cannot be pushed straight to our production environments. All development must occur in isolated staging branches, subject to review by our internal Product Lead.
* **No Hardcoded Keys:** The development company is strictly prohibited from hardcoding server passwords, database credentials, or third-party API tokens directly into the source code. All secrets must be fed dynamically using environment variables or a secure cloud key vault.

### 2.2 Cloud Infrastructure Providers (AWS/GCP) (Control A.5.21 & A.5.22)
Because we operate a cloud-native music distribution platform, our hosting partners must maintain the highest security credentials:
* **Industry Certifications:** We only host our core ingestion engines and artist databases with enterprise-grade cloud partners who maintain active ISO 27001 and SOC 2 Type II compliance certificates.
* **Service Level Agreements (SLAs):** We monitor cloud system uptimes continuously. If a provider's availability dips below our agreed threshold, automated failover loops must instantly redirect traffic to a backup zone to prevent distribution downtime.

---

## 3. Reviewing Partner Security (Control A.5.23)
We don't just take our vendors' word for it. The team manages risk through simple, continuous checks:
1. **Access Revocation:** The moment an external developer leaves the project or our contract with the agency concludes, their repository access keys, database accounts, and communications profiles must be completely deleted within 24 hours.
2. **Annual Check-ins:** Once a year, the GRC Lead will review the security standing of our critical vendors. This involves verifying that their compliance certificates are still valid and ensuring no major security flaws were uncovered in their software dependencies over the past 12 months.
