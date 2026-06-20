# YZB-POL-01: Information Asset Management & Classification Policy

**Document Reference:** YZB-POL-01-2026-V1  
**Classification:** Internal Use Only  
**Effective Date:** June 20, 2026  
**Version:** 1.0  
**Owner:** Director / Product Lead  

---

## 1. Purpose
The purpose of this policy is to identify, inventory, and classify Yearzbuddy’s information assets to guarantee an appropriate level of protection in accordance with **ISO/IEC 27001:2022 Controls A.5.9 and A.5.12**.

## 2. Scope
This policy applies universally to all digital assets, platform codebases, infrastructure endpoints, and operational teams handling intellectual property under Yearzbuddy Technologies Limited.

## 3. Asset Inventory Management (Control A.5.9)
1. All corporate and operational information assets must be explicitly recorded within the master **Yearzbuddy Asset Register**.
2. Every inventory asset must have a designated **Risk Owner** responsible for enforcing lifecycle security controls.
3. The inventory registry must undergo a comprehensive validation review at least once every calendar year.

## 4. Information Classification Scheme (Control A.5.12)
Yearzbuddy assets are classified under a strict four-tier matrix to guide handling requirements:

### 🟥 Tier 1: Highly Confidential
* **Definition:** High-value corporate intellectual property or sensitive consumer data which, if compromised, would cause extreme financial, legal, or reputational damage.
* **Examples:** Unreleased master audio recordings (`.wav`/`.flac`), artist bank routing details, BVN verification sheets.
* **Handling Requirement:** Must be encrypted at rest using AES-256. Access restricted strictly via explicit Role-Based Access Control (RBAC).

### 🟨 Tier 2: Confidential
* **Definition:** Internal business logs or partner details not meant for public viewing.
* **Examples:** Distribution contracts, split-sheets, active metadata repositories (ISRC/UPC logs).
* **Handling Requirement:** Access allowed only to authenticated administrative staff. Sharing requires a valid Non-Disclosure Agreement (NDA).

### 🟦 Tier 3: Internal Use
* **Definition:** General internal documentation that poses minimal operational risk if shared within the corporate bounds.
* **Examples:** Standard operational procedures, training guides, blank compliance templates.
* **Handling Requirement:** Locked behind team authentication; cannot be posted publicly.

### 🟩 Tier 4: Public
* **Definition:** Information formally cleared by management for distribution to the open market.
* **Examples:** Live streaming links, marketing graphics, public press releases.
* **Handling Requirement:** Free distribution. No specific security constraints required.

---

## 5. Information Labeling & Deletion Rules (Controls A.5.13 & A.8.10)
1. **Automated Labeling:** The Yearzbuddy ingestion pipeline must automatically tag raw content repositories with their respective classification identifiers upon upload.
2. **Definitive Information Deletion:** If a distribution contract is terminated or an artist exercises their right to data deletion, all matching Tier 1 audio blocks must be completely purged from the staging buckets within 14 business days.
