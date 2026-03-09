---

# Identity Architecture Design

## Overview

This document describes the identity architecture used to secure access to organisational resources within a **Microsoft 365** environment. The architecture is designed to ensure that all users authenticate through a central identity platform before accessing corporate services.

**Microsoft Entra ID** functions as the primary identity provider in this environment. It manages user authentication, enforces access policies, and evaluates security signals before allowing access to applications and services.

By centralising authentication and access control, the architecture strengthens security while providing a consistent identity management framework.

---

# Architecture Components

The identity architecture consists of several key components that work together to secure access to organisational resources.

---

## Users

Users represent identities within the organisation that require access to business applications and services.

Example user roles in this environment include:

* **Admin User** – Responsible for managing identity services and administrative configurations.
* **HR User** – Accesses human resources systems and internal documentation.
* **Engineering User** – Uses collaboration and development tools for technical work.

Each user authenticates through the identity provider before accessing protected resources.

---

## Identity Provider

**Microsoft Entra ID** serves as the central identity provider responsible for managing authentication and access control across the environment.

Core identity services include:

* **User Authentication** – Verifies user credentials before granting access.
* **Role-Based Access Control (RBAC)** – Assigns permissions based on user roles and responsibilities.
* **Conditional Access Enforcement** – Evaluates contextual security signals before allowing resource access.

This centralised identity model ensures consistent policy enforcement across the organisation.

---

# Security Controls

To strengthen the security posture of the environment, several identity protection mechanisms are implemented.

### Multi-Factor Authentication (MFA)

Multi-factor authentication requires users to verify their identity using an additional authentication factor beyond their password. This significantly reduces the risk of credential compromise.

### Conditional Access Policies

Conditional Access policies evaluate multiple conditions before granting access. These conditions may include user identity, device status, location, or risk level.

These policies are configured and enforced through **Microsoft Entra ID**.

### Identity Governance Using RBAC

Role-Based Access Control ensures that users receive only the permissions necessary for their roles. Administrative privileges are restricted to authorised personnel to reduce the risk of privilege misuse.

---

# Microsoft 365 Services

Once authenticated, users may access a variety of organisational services hosted within **Microsoft 365**.

Examples of protected services include:

* **Exchange Online** – Email and messaging services
* **SharePoint Online** – Document management and collaboration platform
* **Microsoft Teams** – Communication and collaboration workspace

Access to these services is controlled through authentication and access policies configured within **Microsoft Entra ID**.

---

# Access Flow

A typical authentication and access flow within the architecture occurs as follows:

1. A user attempts to access a Microsoft 365 service.
2. The authentication request is redirected to **Microsoft Entra ID**.
3. The identity provider verifies the user's credentials.
4. Security controls such as **Multi-Factor Authentication** and **Conditional Access policies** are evaluated.
5. If all conditions are satisfied, access to the requested service is granted.

This process ensures that every access request is validated before organisational resources are accessed.

---

# Summary

This identity architecture establishes **Microsoft Entra ID** as the central authentication and access control platform for the organisation. By implementing strong authentication, role-based permissions, and Conditional Access policies, the environment ensures that only authorised users can access sensitive resources.

The architecture provides a secure and scalable identity framework for managing access to services within **Microsoft 365**.


















Identity Architecture Design
Overview

Identity serves as the primary security boundary in modern cloud environments. In Microsoft 365, authentication determines whether users are permitted to access organisational resources regardless of their location, device, or network.

This architecture establishes Microsoft Entra ID as the central identity provider responsible for authentication, authorization, and identity governance across the environment.

All authentication requests pass through the identity platform before access to Microsoft 365 workloads is granted.

The architecture supports a Zero Trust security model, where authentication attempts are continuously evaluated using identity signals, device posture, and contextual risk indicators before access is granted.

Identity Platform
Microsoft Entra ID

Microsoft Entra ID functions as the organisation’s identity provider and authentication platform.

Core responsibilities include:

User authentication and identity verification

Role-Based Access Control (RBAC)

Conditional Access policy enforcement

Identity risk detection

Token issuance for Microsoft 365 services

By centralising identity services within Entra ID, organisations maintain a consistent authentication framework across cloud services.

Identity Types

The environment supports several identity types that interact with Microsoft 365 resources.

Administrative Users

Administrative identities manage identity services, security policies, and tenant configuration.

Examples of administrative roles include:

Global Administrator

Security Administrator

User Administrator

Because these accounts have elevated privileges, they require strong authentication protection and privileged access governance.

Standard Employee Identities

Employee identities represent internal users accessing collaboration services and productivity applications.

Typical resources accessed include:

Exchange Online

SharePoint Online

Microsoft Teams

OneDrive for Business

These users authenticate through Microsoft Entra ID before accessing organisational resources.

Guest Users

Guest identities allow external partners or collaborators to access shared resources within the Microsoft 365 environment.

Guest access is managed using Microsoft Entra B2B collaboration and controlled through Conditional Access policies.

This allows organisations to securely collaborate with external users while maintaining control over resource access.

Service Accounts

Service identities represent automated services, applications, or scripts that require authentication to interact with organisational resources.

Examples include:

Automation scripts

Application integrations

Background services

These identities are carefully restricted and monitored to reduce the risk of misuse.

Identity Integration with Security Services

The identity platform integrates with multiple Microsoft security services to strengthen authentication and access decisions.

Microsoft Intune

Microsoft Intune provides device compliance and endpoint posture signals that are evaluated during Conditional Access authentication decisions.

Microsoft Defender

Microsoft Defender services provide threat intelligence and risk signals related to identity and endpoint activity.

These signals can influence authentication decisions when suspicious behaviour is detected.

Microsoft Purview

Microsoft Purview ensures that sensitive data accessed through authenticated sessions remains protected through classification and policy enforcement.

Authentication Flow

A typical authentication and access flow occurs as follows:

A user attempts to access a Microsoft 365 service.

The authentication request is redirected to Microsoft Entra ID.

The identity provider verifies the user's credentials.

Conditional Access policies evaluate authentication signals such as:

Device compliance

User location

Identity risk level

If required, Multi-Factor Authentication is triggered.

If all policy conditions are satisfied, an authentication token is issued.

The user gains access to the requested Microsoft 365 service.

This process ensures that every access request is evaluated before organisational resources are accessed.

Identity Security Model

The architecture follows several identity security principles.

Identity as the Security Boundary

Access decisions originate from identity verification rather than network location.

Strong Authentication

Authentication security is strengthened through Multi-Factor Authentication and risk-based authentication.

Policy-Based Access Control

Conditional Access policies enforce contextual access decisions based on identity and device signals.

Continuous Monitoring

Authentication activity and identity behaviour are continuously monitored to detect potential threats.

Summary

This identity architecture establishes Microsoft Entra ID as the central authentication and identity governance platform for the organisation.

By combining strong authentication, identity governance, device compliance validation, and threat intelligence, the environment creates a secure identity framework that protects access to Microsoft 365 services.

