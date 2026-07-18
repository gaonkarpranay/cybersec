# Phase 3 – Conduct Penetration Test

## Objective

Validate the effectiveness of the remediation actions by performing a **penetration test**, ensuring that the Linux server is:

- Secure
- Properly remediated
- Compliant with the organization's security policy

---

# 1. Execution

The penetration test is performed to verify whether the implemented security controls effectively protect the Linux server.

## Network Scan

### Tool

- **Nmap**

### Purpose

Identify:

- Open ports
- Running services
- Service versions
- Potential attack surface

---

## Vulnerability Scanning

### Tool

- **Metasploit**

### Purpose

- Identify known vulnerabilities.
- Attempt to exploit discovered vulnerabilities.
- Verify whether remediation efforts have successfully eliminated the identified weaknesses.

---

## Web Application Testing

### Tool

- **Burp Suite** (if applicable)

### Purpose

Assess the security of hosted web applications by testing for common web vulnerabilities and validating implemented security controls.

---

# 2. Validating Remediation

After completing the penetration test, verify whether the remediation efforts were successful.

## Compare Results

Compare:

- Initial security audit findings
- Penetration testing results

This helps confirm that previously identified vulnerabilities have been successfully remediated.

---

## Check for New Vulnerabilities

Determine whether any new vulnerabilities were introduced during the remediation process.

If new issues are identified:

- Document them.
- Prioritize remediation.
- Recommend appropriate security improvements.

---

# 3. Reporting

Document all findings and provide actionable recommendations.

## Executive Summary

Provide a high-level overview including:

- Purpose of the penetration test
- Overall security posture
- Major findings
- Overall conclusion

---

## Methodology

Document the testing methodology, including:

- Tools used
- Testing techniques
- Scope of assessment
- Testing approach

---

## Findings

For each identified vulnerability, include:

- Description
- Severity
- Potential impact
- Affected systems
- Supporting evidence (if applicable)

---

## Recommendations

Provide actionable recommendations to:

- Eliminate identified vulnerabilities.
- Improve system security.
- Strengthen security controls.
- Maintain compliance with the organization's security policy.

---

# Penetration Testing Workflow

```text
Security Audit
      │
      ▼
Remediation Implemented
      │
      ▼
Conduct Penetration Test
      │
      ├── Network Scan (Nmap)
      ├── Vulnerability Scanning (Metasploit)
      └── Web Application Testing (Burp Suite)
      │
      ▼
Validate Remediation
      │
      ├── Compare with Audit Findings
      └── Identify New Vulnerabilities
      │
      ▼
Generate Report
      │
      ├── Executive Summary
      ├── Methodology
      ├── Findings
      └── Recommendations
      │
      ▼
Further Remediation & Continuous Improvement
```

---

> **Key Takeaway**
>
> The **Security Audit** identifies policy, compliance, and configuration weaknesses, while the **Penetration Test** verifies whether those weaknesses have been effectively remediated and determines if they can still be exploited. Together, they provide a comprehensive assessment of an organization's security posture.