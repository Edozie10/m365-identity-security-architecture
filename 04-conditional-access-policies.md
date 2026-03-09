# Conditional Access Policies

---

# Overview

**Conditional Access** provides a dynamic security layer that evaluates multiple conditions before granting access to organisational resources.

Instead of relying solely on static authentication requirements, Conditional Access evaluates contextual signals such as **user identity, device compliance, location, and risk level**.

Within this environment, Conditional Access policies are configured through **Microsoft Entra ID** to protect services hosted within **Microsoft 365**.

By enforcing security controls at the authentication stage, Conditional Access ensures that only **authorised users with trusted devices and verified identities** can access sensitive organisational resources.

---

# Policy Evaluation Criteria

Conditional Access policies evaluate several security signals before allowing access to an application or service.

Typical evaluation factors include:

* **User Identity** – The identity requesting access
* **Authentication Strength** – Whether strong authentication methods such as MFA are used
* **Device Compliance** – Whether the device meets organisational security requirements
* **Location** – The geographic or network location of the access request
* **Identity Risk Level** – Risk signals detected by Microsoft Entra ID Identity Protection

These conditions allow administrators to enforce **context-aware access decisions**.

---

# Implemented Conditional Access Policies

Several Conditional Access policies are implemented to strengthen the organisation’s identity security posture.

---

### Require MFA for Administrators

Administrative accounts hold elevated privileges and therefore require stronger authentication protection.

This policy ensures that all users assigned **administrative roles within Microsoft Entra ID** must complete **Multi-Factor Authentication (MFA)** before accessing administrative services.

Key objectives include:

* **Protecting privileged accounts from credential compromise**
* **Reducing the risk of unauthorized administrative access**
* **Strengthening overall tenant security**

---

### Require MFA for External Access

Users accessing organisational resources from **outside the corporate network** must verify their identity using Multi-Factor Authentication.

This policy ensures that remote access to Microsoft 365 services requires an additional authentication factor.

This helps mitigate risks associated with:

* Untrusted networks
* Credential theft
* Remote access attacks

---

### Require Compliant Device

Access to sensitive organisational resources is restricted to devices that meet defined security standards.

Device compliance information is evaluated through **Microsoft Intune**, which verifies that devices follow organisational security policies.

Compliance checks may include:

* Device encryption status
* Operating system security updates
* Endpoint protection configuration
* Device enrollment in Microsoft Intune

If a device does not meet compliance requirements, access to protected resources may be restricted or denied.

---

### Block High-Risk Sign-Ins

Conditional Access policies may block authentication attempts that are identified as **high risk** by Microsoft Entra ID Identity Protection.

Examples of high-risk scenarios include:

* Sign-ins from unfamiliar locations
* Suspicious login behaviour
* Potential credential compromise

Blocking high-risk authentication attempts helps prevent attackers from gaining access using stolen credentials.

---

# Security Benefits

Conditional Access policies significantly improve the organisation’s security posture by enforcing **context-based access controls**.

---

### Stronger Authentication Protection

MFA requirements ensure that user identities are verified using **multiple authentication factors**.

---

### Reduced Risk of Unauthorized Access

Context-aware access decisions prevent attackers from accessing resources using **compromised credentials or untrusted devices**.

---

### Device Security Enforcement

Requiring **compliant devices through Microsoft Intune** ensures that only properly managed and secure devices can access sensitive systems.

---

### Adaptive Access Control

Conditional Access allows organisations to dynamically adapt security controls based on authentication signals and risk indicators.

---

# Relationship to Identity Security Architecture

Conditional Access acts as the **policy enforcement engine** within the identity security architecture.

Authentication requests are processed through **Microsoft Entra ID**, where policies evaluate identity signals, device posture, and contextual conditions before granting access to Microsoft 365 services.

These policies work together with:

* **Multi-Factor Authentication**
* **Identity Governance**
* **Microsoft Intune device compliance**
* **Microsoft Defender risk signals**

Together, these controls create a **layered Zero Trust security model**.

---

# Summary

Conditional Access policies strengthen identity security by introducing **context-aware access controls** that evaluate authentication conditions before granting access.

By leveraging the capabilities of **Microsoft Entra ID and Microsoft Intune**, the organisation ensures that only verified users, trusted devices, and secure access scenarios can reach sensitive resources within Microsoft 365.

This approach significantly enhances the organisation’s overall security posture.
