# YZB-POL-03: Information Security Incident Response Plan

**Document Reference:** YZB-POL-03-2026-V1  
**Classification:** Internal Use Only  
**Effective Date:** June 20, 2026  
**Version:** 1.0  
**Owner:** Security Manager / GRC Compliance Lead  

---

## 1. What This Policy Is About
At Yearzbuddy, an "incident" isn't just a hypothetical IT bug—it's any real-world event that threatens our data, our platform, or our artists' trust. This includes a data breach, an unauthorized server login, or a music leak where an unreleased master track gets exposed online before its official drop date. 

This policy explains exactly who does what when things go wrong, how we fix problems fast, and how we meet our strict 72-hour regulatory notification deadlines under **ISO/IEC 27001:2022 (Controls A.5.24 - A.5.28)**.

## 2. Who is Responsible?
Because we operate as a lean, focused team, we don't have layers of corporate committees. Responsibilities are split clearly to avoid confusion during an emergency:
* **Security Manager / GRC Lead:** Leads the containment strategy, coordinates the technical response, preserves digital evidence, and manages official legal or regulatory reports.
* **Product & Engineering Lead:** Shuts down compromised code deployment branches, locks out breached cloud infrastructure keys (AWS/GCP), and fixes the underlying technical security flaws.
* **Director:** Handles direct communication with affected music clients, distribution partners, and international streaming platforms (DSPs) if an impact occurs.

---

## 3. The 4-Step Emergency Playbook

When a vulnerability or leak is reported, the team drops non-essential operational tasks and immediately moves through these four phases:

### Phase 1: Identification & Sorting (Control A.5.25)
Anyone on the team who spots a security anomaly must immediately email **security@yearzbuddy.com**. We categorize the emergency level into one of two clear buckets:
* **Low/Medium Priority:** A single user dashboard is acting up, or a team member lost a corporate device that was already fully encrypted and locked down remotely.
* **High Priority (Critical):** Any sign of unauthorized database access, altered royalty routing files, or a leak involving an unreleased master recording file (`.wav`/`.flac`).

### Phase 2: Containment & Isolation (Control A.5.26)
We prioritize stopping the bleeding over figuring out who is to blame.
* If an administrative account is compromised, the Engineering Lead instantly revokes its active API tokens and enforces a global password reset.
* If a storage bucket is leaking music, the access control permissions are instantly flipped to private, isolating the server environment from the open internet.

### Phase 3: Investigation & The 72-Hour Clock (Control A.5.27)
* **The Regulatory Rule:** If personal identity details or financial data belong to clients under data protection laws, the Security Manager must formally document and report the incident to authorities within **72 hours** of discovery.
* **Evidence Handling:** The team must log system timeline records and keep server snapshots completely unaltered. We never delete historical logs during an active investigation, ensuring we have a clean trail to analyze.

### Phase 4: Fixing & Retrospectives (Control A.5.28)
An incident is only truly closed when we ensure it cannot happen again. Within 5 business days of resolving a major issue, the team holds an informal post-mortem meeting to ask: *What broke? Why did our baseline controls miss it? How do we update our software deployment checklists to immunize our platform from this specific attack vector moving forward?*
