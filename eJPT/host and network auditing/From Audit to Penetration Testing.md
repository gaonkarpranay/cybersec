# From Audit to Penetration Testing

This section demonstrates, through a practical example, **how security audits are performed**, **how they influence penetration testing**, and **how audit findings shape the scope and objectives of a penetration test**.

The goal is to understand:

- How security audits work.
- How security audits relate to penetration testing.
- How audit findings affect the objectives and scope of a penetration test.
- The changes and adaptations required when performing a penetration test for organizations that must comply with specific standards or regulations.

---

# Practical Scenario

## Company Background

**Company:** SecureTech Solutions

### Description

**SecureTech Solutions** is a fictitious cybersecurity consultancy specializing in securing IT infrastructure for various clients.

In this example, the organization will:

- Develop a security policy for Linux servers.
- Perform a risk assessment using the **NIST SP 800-53** framework.
- Conduct a security audit.
- Test the implemented remediations through penetration testing.

This practical example demonstrates the complete security assessment lifecycle—from policy creation to penetration testing—while emphasizing the importance of regulatory compliance.

---

# Phase 1 – Developing a Security Policy

## Objectives

The primary objective is to establish a **baseline security policy** for Linux servers aligned with **NIST SP 800-53**.

The policy aims to:

- Ensure Linux servers are securely configured and managed.
- Protect servers from unauthorized access.
- Reduce vulnerabilities and security threats.
- Establish baseline security requirements for configuring, maintaining, and monitoring Linux servers.

---

# Security Policy Development Process

## Requirements Gathering

Before writing the security policy, identify the organization's security requirements.

### Areas to Define

### Purpose

- Define the purpose and scope of the security policy.

### Access Control

- User account management.
- Authentication methods.
- Privilege management.

### Audit and Accountability

- Logging requirements.
- Log review procedures.

### Configuration Management

- Baseline system configurations.
- Software update practices.
- Change management procedures.

### Identification and Authentication

- Strong password policies.
- Unique user identification.

### System and Information Integrity

- Malware protection.
- Security monitoring.
- Vulnerability management.

### Maintenance

- Controlled maintenance procedures.
- Approved maintenance tools.

---

# Simple Security Policy for Linux Servers (Aligned with NIST SP 800-53)

## Access Control (AC)

| Policy Area | Control ID | Policy Statement |
|-------------|------------|------------------|
| **Access Control (AC)** | **AC-2, AC-5** | **User Accounts:** Only authorized personnel shall be granted access to Linux servers. Each user must have a unique user account. Shared accounts are prohibited. Inactive accounts must be disabled or removed within **30 days**. |
| | **IA-2, IA-5** | **Authentication:** Enforce strong password policies with a minimum length of **12 characters**, including uppercase letters, lowercase letters, numbers, and special characters. Use **SSH key-based authentication** whenever possible and disable password-based SSH access. Implement **Two-Factor Authentication (2FA)** for privileged accounts. |

---

## Audit and Accountability (AU)

| Policy Area | Control ID | Policy Statement |
|-------------|------------|------------------|
| **Audit and Accountability (AU)** | **AU-2, AU-3** | **System Logging:** Enable and configure system logging to capture critical security events. Use **rsyslog** or **journald** for centralized logging. |
| | **AU-6, AU-7** | **Log Review:** Regularly review system logs for suspicious activity and retain logs for a minimum of **90 days**. |

---

## Configuration Management (CM)

| Policy Area | Control ID | Policy Statement |
|-------------|------------|------------------|
| **Configuration Management (CM)** | **CM-2** | **Configuration Baseline:** Maintain a secure baseline configuration for all Linux servers. Use configuration management tools such as **Ansible** or **Puppet** to enforce secure configurations. |
| | **CM-3, CM-5** | **Software Updates:** Keep the operating system and installed software up to date. Apply security patches within **30 days** of release. |

---

## Identification and Authentication (IA)

| Policy Area | Control ID | Policy Statement |
|-------------|------------|------------------|
| **Identification and Authentication (IA)** | **IA-5** | **Password Management:** Enforce password complexity and password expiration policies. Use password managers to securely store and manage passwords. |
| | **IA-4** | **User Identification:** Ensure that every user has a unique identity within the system. |

---

## System and Information Integrity (SI)

| Policy Area | Control ID | Policy Statement |
|-------------|------------|------------------|
| **System and Information Integrity (SI)** | **SI-3** | **Malware Protection:** Implement malware detection and prevention measures. Perform regular malware scans on Linux servers. |
| | **SI-4** | **Security Monitoring:** Continuously monitor systems for security breaches and anomalies. Use tools such as **Lynis** to perform regular security audits. |

---

## Maintenance (MA)

| Policy Area | Control ID | Policy Statement |
|-------------|------------|------------------|
| **Maintenance (MA)** | **MA-2** | **Controlled Maintenance:** Perform server maintenance according to documented procedures. |
| | **MA-3** | **Maintenance Tools:** Use only approved and trusted maintenance tools and ensure they are securely managed. |

---

> **Key Takeaway**
>
> Before conducting a security audit or penetration test, an organization should establish a well-defined **security policy**. This policy serves as the baseline against which systems are audited and provides the security controls that penetration testers later validate through technical testing.