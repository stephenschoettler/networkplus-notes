## 💡 Playbooks (OBJ 1.8)

Playbooks are documented specific actions for emergency scenarios/incidents (checklist). Their purpose is to prepare for incident response, ensure documented procedures, and enable quick response. They often follow NIST incident response process phases.

✅ **Runbooks**
- **Definition:** Automated version of a playbook (partially or fully automated).
- **Purpose:** Gain efficiencies, free up analysts for higher-level work.
- **SOAR (Security Orchestration, Automation, and Response) Systems:**
  - Tools that orchestrate and automate runbooks for incident response, threat hunting, etc.
  - Can automate provisioning, account management, re-imaging, etc.

✅ **Common Playbook/Runbook Types**
- **1. Ransomware Playbook:**
  - **Focus:** Isolate/disconnect networks quickly (do NOT power off infected systems).
- **2. Data Exfiltration Playbook:**
  - **Focus:** Stop ongoing exfiltration, protect data stores, forensic analysis.
- **3. Social Engineering (Phishing) Playbook:**
  - **Focus:** Identify affected users, reset passwords, re-image, analyze emails in sandbox.