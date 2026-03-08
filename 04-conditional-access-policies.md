---

# Conditional Access Policies

## Overview

Conditional Access policies provide a dynamic security layer that evaluates multiple conditions before granting access to organisational resources. Instead of relying solely on static authentication requirements, these policies assess contextual signals such as user identity, device status, and location.

Within this environment, Conditional Access policies are configured through **Microsoft Entra ID** to protect services hosted in **Microsoft 365**.

By enforcing security controls at the authentication stage, Conditional Access helps ensure that only authorised users with trusted devices can access sensitive resources.

---

# Policy Evaluation Criteria

Conditional Access policies evaluate several signals before allowing access to an application or service.

Typical evaluation factors include:

* **User identity** – The identity requesting access
* **Authentication strength** – Whether strong authentication methods are used
* **Device compliance** – Whether the device meets security standards
* **Location** – The geographic or network location of the access request

These conditions allow administrators to enforce context-aware access decisions.

---

# Implemented Conditional Access Policies

The following policies are implemented within the environment.

---

## Require MFA for Administrators

Administrative accounts hold elevated privileges and therefore require stronger authentication protection.

This policy ensures that all users assigned administrative roles within **Microsoft Entra ID** must complete **Multi-Factor Authentication (MFA)** before accessing administrative services.

Key objectives include:

* Protecting privileged accounts from credential compromise
* Reducing the risk of unauthorized administrative access
* Strengthening overall tenant security

---

## Require MFA for External Access

Users accessing services from outside the corporate network must verify their identity using Multi-Factor Authentication.

This policy ensures that external access to organisational services hosted in **Microsoft 365** requires an additional authentication factor.

This helps mitigate risks associated with remote access and untrusted networks.

---

## Require Compliant Device

Access to sensitive organisational resources is restricted to devices that meet defined compliance standards.

Device compliance information is evaluated through **Microsoft Intune**, which verifies that devices follow the organisation's security policies.

If a device does not meet compliance requirements, access to protected resources may be restricted or denied.

---

# Security Benefits

Conditional Access policies significantly improve the organisation’s security posture by enforcing context-based access controls.

### Stronger Authentication Protection

MFA requirements ensure that user identities are verified using multiple authentication factors.

### Reduced Risk of Unauthorized Access

Context-aware access decisions help prevent attackers from accessing resources using compromised credentials.

### Device Security Enforcement

Requiring compliant devices ensures that only secure and properly managed devices can access sensitive systems.

---

# Relationship to Identity Security Architecture

Conditional Access operates as a central enforcement mechanism within the identity architecture.

Authentication requests are processed through **Microsoft Entra ID**, where policies evaluate identity and security signals before granting access to services hosted within **Microsoft 365**.

These policies work together with Multi-Factor Authentication and identity governance controls to create a layered security model.

---

# Summary

Conditional Access policies strengthen identity security by introducing context-aware access controls that evaluate authentication conditions before granting access.

By leveraging the capabilities of **Microsoft Entra ID**, the organisation ensures that only verified users, trusted devices, and secure access scenarios are allowed to reach sensitive resources within **Microsoft 365**.

This approach significantly enhances the organisation’s overall security posture.
