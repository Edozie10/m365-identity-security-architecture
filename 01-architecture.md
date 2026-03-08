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

