# Identity Architecture Design

---

# Overview

Identity serves as the **primary security boundary** in modern cloud environments. In Microsoft 365, authentication determines whether users are permitted to access organisational resources regardless of their location, device, or network.

This architecture establishes **Microsoft Entra ID** as the central identity provider responsible for authentication, authorization, and identity governance across the environment.

All authentication requests pass through the identity platform before access to Microsoft 365 workloads is granted.

The architecture follows a **Zero Trust security model**, where authentication attempts are continuously evaluated using identity signals, device posture, and contextual risk indicators.

---

# Identity Platform

---

### Microsoft Entra ID

**Microsoft Entra ID** functions as the organisation’s identity provider and authentication platform.

Core responsibilities include:

* **User authentication and identity verification**
* **Role-Based Access Control (RBAC)**
* **Conditional Access policy enforcement**
* **Identity risk detection**
* **Token issuance for Microsoft 365 services**

Centralising identity services within Entra ID ensures consistent authentication policies across the organisation.

---

# Identity Types

The environment supports several identity types that interact with Microsoft 365 services.

---

### Administrative Users

Administrative identities manage identity services, security configuration, and tenant administration.

Examples include:

* **Global Administrator**
* **Security Administrator**
* **User Administrator**

Because these accounts have elevated privileges, they require:

* **Multi-Factor Authentication**
* **Privileged access governance**
* **Continuous monitoring**

---

### Standard Employee Identities

Employee identities represent internal users accessing organisational services.

Typical services accessed include:

* **Exchange Online**
* **SharePoint Online**
* **Microsoft Teams**
* **OneDrive for Business**

These users authenticate through **Microsoft Entra ID** before accessing organisational resources.

---

### Guest Users

Guest identities allow external partners or collaborators to access shared organisational resources.

Guest access is managed using **Microsoft Entra B2B collaboration** and controlled through **Conditional Access policies**.

---

### Service Accounts

Service accounts represent automated services or applications that require authentication to interact with Microsoft 365 resources.

Examples include:

* Automation scripts
* Application integrations
* Background services

These identities are carefully restricted and monitored.

---

# Identity Integration with Security Services

---

### Microsoft Intune

**Microsoft Intune** provides **device compliance and endpoint posture signals** that are evaluated during Conditional Access authentication decisions.

Examples include:

* Device compliance status
* Operating system security configuration
* Endpoint health signals

---

### Microsoft Defender

**Microsoft Defender services** provide threat intelligence and behavioural monitoring across identities and endpoints.

These signals may influence Conditional Access decisions when suspicious activity is detected.

---

### Microsoft Purview

**Microsoft Purview** protects organisational data accessed during authenticated sessions.

Capabilities include:

* Data classification
* Sensitivity labels
* Data Loss Prevention policies

---

# Authentication Flow

A typical authentication process follows these steps:

1. A user attempts to access a Microsoft 365 service.

2. The authentication request is redirected to **Microsoft Entra ID**.

3. User credentials are verified by the identity provider.

4. **Conditional Access policies** evaluate authentication signals including:

   * Device compliance
   * User location
   * Identity risk level

5. If required, **Multi-Factor Authentication** is triggered.

6. If policy requirements are satisfied, an authentication token is issued.

7. The user gains access to the requested Microsoft 365 service.

---

# Identity Security Model

The architecture follows several key security principles.

### Identity as the Security Boundary

Access decisions originate from **identity verification rather than network location**.

### Strong Authentication

Authentication security is strengthened through **Multi-Factor Authentication and risk-based authentication**.

### Policy-Based Access Control

Conditional Access policies enforce **context-aware access decisions**.

### Continuous Monitoring

Authentication activity and identity behaviour are continuously monitored for suspicious activity.

---

# Summary

This identity architecture establishes **Microsoft Entra ID** as the central authentication and identity governance platform for the organisation.

By combining **strong authentication, device compliance validation, identity governance, and threat detection**, the architecture provides a secure foundation for accessing Microsoft 365 services.
