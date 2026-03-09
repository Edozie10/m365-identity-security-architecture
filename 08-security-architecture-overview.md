# Security Architecture Overview

---

# Overview

This document provides a high-level overview of the **Microsoft 365 Zero Trust security architecture** implemented within this environment.

The architecture is designed around Microsoft's **Zero Trust security model**, where every authentication attempt is evaluated based on identity, device posture, and security signals before access to organisational resources is granted.

Rather than relying on traditional network-based security boundaries, this architecture focuses on **identity-driven access control** supported by layered security technologies across Microsoft 365.

The architecture integrates several Microsoft security platforms to provide protection across:

* **Identities**
* **Devices**
* **Applications**
* **Organisational Data**

---

# Core Security Architecture Layers

The architecture is organised into four primary security layers aligned with Microsoft's Zero Trust model.

---

### Identity Layer — Microsoft Entra ID

**Microsoft Entra ID** serves as the central identity provider responsible for authentication and access control.

Key capabilities include:

* **User authentication and identity verification**
* **Role-Based Access Control (RBAC)**
* **Conditional Access policy enforcement**
* **Identity risk detection**
* **Privileged Identity Management (PIM)**

All authentication requests must pass through Microsoft Entra ID before users can access Microsoft 365 services.

---

### Device Security Layer — Microsoft Intune

**Microsoft Intune** provides endpoint management and device security enforcement.

Devices accessing organisational resources must meet defined compliance requirements before access is granted.

Key capabilities include:

* **Device enrollment and management**
* **Mobile Device Management (MDM)**
* **Mobile Application Management (MAM)**
* **Device compliance evaluation**

Device compliance signals are used by **Conditional Access policies** during authentication decisions.

---

### Threat Protection Layer — Microsoft Defender

The **Microsoft Defender security platform** provides advanced threat detection across identities, endpoints, and email services.

Key Defender services include:

* **Microsoft Defender for Endpoint**
* **Microsoft Defender for Identity**
* **Microsoft Defender for Office 365**
* **Microsoft Defender for Cloud Apps**

These services provide continuous monitoring and detection of suspicious behaviour across the Microsoft 365 environment.

---

### Data Protection Layer — Microsoft Purview

**Microsoft Purview** provides data protection and compliance capabilities across organisational workloads.

Key features include:

* **Sensitivity labels and data classification**
* **Data Loss Prevention (DLP) policies**
* **Insider Risk Management**
* **eDiscovery and compliance tools**

These capabilities ensure that sensitive organisational information remains protected regardless of where it is stored or shared.

---

# Microsoft 365 Workloads Protected

This architecture protects several core Microsoft 365 services including:

* **Exchange Online**
* **SharePoint Online**
* **Microsoft Teams**
* **OneDrive for Business**

Access to these workloads is controlled through authentication policies and device security enforcement.

---

# Zero Trust Security Principles

This architecture follows several core Zero Trust principles.

---

### Verify Explicitly

Every authentication request is evaluated using identity signals, device posture, and contextual risk indicators.

---

### Least Privilege Access

Users are granted only the permissions necessary to perform their roles.

---

### Assume Breach

Security monitoring tools continuously observe authentication behaviour and system activity to detect potential threats.

---

# Summary

This Microsoft 365 security architecture integrates **identity protection, device security, threat detection, and data protection** into a unified security framework.

By combining **Microsoft Entra ID, Microsoft Intune, Microsoft Defender, and Microsoft Purview**, the organisation implements a layered security model aligned with **Zero Trust principles**.
