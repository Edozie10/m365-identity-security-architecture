# Multi-Factor Authentication Implementation

---

# Overview

**Multi-Factor Authentication (MFA)** adds an additional layer of security by requiring users to verify their identity using more than one authentication factor.

Instead of relying solely on passwords, MFA combines something the user **knows** with something the user **possesses** or can **verify**.

Within this environment, MFA is implemented through **Microsoft Entra ID** to strengthen authentication security for users accessing services within **Microsoft 365**.

By requiring multiple authentication factors, the system significantly reduces the risk of unauthorized access caused by compromised credentials.

---

# MFA Authentication Methods

Users can authenticate using several verification methods supported by **Microsoft Entra ID**.

---

### Microsoft Authenticator App

The **Microsoft Authenticator application** allows users to approve authentication requests using push notifications or verification codes generated on their mobile device.

This method provides a **convenient and secure way** for users to complete authentication challenges.

Benefits include:

* **Push notification approval**
* **Time-based verification codes**
* **Support for passwordless authentication**

---

### SMS Verification

Users receive a **one-time verification code via SMS** to their registered mobile number.

The user must enter this code during the authentication process to confirm their identity.

This method provides a simple authentication option for users without the Microsoft Authenticator application.

---

### Phone Call Verification

During authentication, a **phone call is placed to the user’s registered number**.

The user confirms the login attempt by following the voice instructions provided during the call.

This method provides an additional verification mechanism for users.

---

# MFA Enforcement Strategy

Multi-Factor Authentication is enforced for specific scenarios to protect sensitive accounts and high-risk activities.

---

### Administrative Accounts

All administrative users within **Microsoft Entra ID** are required to authenticate using MFA due to the elevated privileges associated with these roles.

This protects critical administrative accounts from compromise.

---

### Remote Access

Users accessing organisational resources from **external networks** must complete MFA verification before gaining access.

This protects the environment from risks associated with remote access.

---

### High-Risk Sign-In Attempts

If **Microsoft Entra ID Identity Protection** detects unusual or suspicious authentication behaviour, additional verification through MFA may be required before access is granted.

Examples include:

* Unusual sign-in locations
* Suspicious authentication patterns
* Potential credential compromise

---

# Security Benefits

Implementing **Multi-Factor Authentication** provides several important security advantages.

---

### Reduced Credential Risk

Even if a password becomes compromised, attackers cannot access accounts without the **second authentication factor**.

---

### Stronger Identity Verification

Multiple authentication factors improve the reliability of identity verification during login attempts.

---

### Protection Against Phishing Attacks

MFA helps mitigate phishing attacks by requiring an additional authentication step beyond captured credentials.

---

# Relationship to Identity Security Architecture

Multi-Factor Authentication operates as a **core security control** within the broader identity architecture.

Authentication requests are processed through **Microsoft Entra ID**, where **Conditional Access policies** determine whether MFA verification is required before granting access to services hosted within Microsoft 365.

This layered authentication model strengthens identity protection and helps enforce secure access policies across the environment.

---

# Summary

Multi-Factor Authentication enhances the security of the identity environment by requiring users to verify their identity using multiple authentication factors.

By integrating **MFA with Microsoft Entra ID**, the organisation significantly reduces the risk of unauthorized access while maintaining secure access to services within Microsoft 365.
