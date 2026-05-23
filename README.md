# FUTURE_CS_01

# Task 1 — Vulnerability Assessment Report for a Live Website

Internship: Future Interns — Cyber Security Track  
Intern: Ahmar Shafith Baijur Ahamed  
Date: May 23 2026  


# Objective

Conduct a passive vulnerability assessment on a legal, intentionally vulnerable demo web application using industry-standard security tools. Identify, classify, and document security vulnerabilities with clear remediation steps.


# Target

| Field | Details |
|-------|---------|
| **URL** | http://zero.webappsecurity.com |
| **Type** | Demo Banking Web Application (HP WebInspect) |
| **IP** | 54.82.22.214 (AWS Hosted) |
| **Server** | Apache Tomcat / Coyote JSP Engine 1.1 |
| **Assessment Type** | Passive Grey-Box Vulnerability Assessment |

---

## 🔧 Tools Used

| Tool | Purpose |
|------|---------|
| **Nmap 7.99** | Port scanning & service version detection |
| **OWASP ZAP** | Passive web vulnerability scanning |
| **Browser DevTools** | HTTP headers, cookies & console inspection |

---

## 📊 Findings Summary

| # | Vulnerability | Risk | CWE |
|---|--------------|------|-----|
| 1 | Content Security Policy (CSP) Header Not Set | 🟠 Medium | CWE-693 |
| 2 | Cross-Domain Misconfiguration (CORS Wildcard) | 🟠 Medium | CWE-264 |
| 3 | Missing Anti-Clickjacking Header (X-Frame-Options) | 🟠 Medium | CWE-1021 |
| 4 | Vulnerable JavaScript Library (jQuery 1.8.2) | 🟠 Medium | CWE-1395 |
| 5 | In-Page Banner Information Leak (Tomcat/7.0.70) | 🟡 Low | CWE-497 |
| 6 | Server Version Disclosure via HTTP Response Header | 🟡 Low | CWE-497 |
| 7 | X-Content-Type-Options Header Missing | 🟡 Low | CWE-693 |
| 8 | Modern Web Application (Informational) | 🔵 Info | — |

---

## 📁 Repository Structure
FUTURE_CS_01/
│
├── README.md
├── report/
│   └── Vulnerability_Assessment_Report_FUTURE_CS_01.pdf
└── screenshots/
├── nmap_basic_scan.png
├── nmap_version_scan.png
├── zap_alerts_overview.png
├── zap_csp_header.png
├── zap_cors_misconfiguration.png
├── zap_clickjacking_header.png
├── zap_vulnerable_js_library.png
├── zap_banner_info_leak.png
├── zap_server_version_disclosure.png
└── zap_xcontent_type_options.png

---

## 🔍 Nmap Scan Results

**Basic Scan:** `nmap zero.webappsecurity.com`
PORT      STATE  SERVICE
80/tcp    open   http
443/tcp   open   https
8080/tcp  open   http-proxy

**Version Scan:** `nmap -sV zero.webappsecurity.com`
PORT      STATE  SERVICE   VERSION
80/tcp    open   http      Apache Tomcat/Coyote JSP engine 1.1
443/tcp   open   ssl/https Apache Tomcat/Coyote JSP engine 1.1
8080/tcp  open   http      Apache Tomcat/Coyote JSP engine 1.1

---

## ⚠️ Legal Disclaimer

This assessment was conducted solely for **educational purposes** as part of the Future Interns Cyber Security Internship (Task 1). The target is a **legal, intentionally vulnerable demo application**. No vulnerabilities were exploited. No real user data was accessed or modified. All scanning was passive and ethical.

---

## 📜 Deliverables

- ✅ Vulnerability Assessment Report (PDF) — in `/report/`
- ✅ Nmap Scan Screenshots — in `/screenshots/`
- ✅ OWASP ZAP Alert Screenshots — in `/screenshots/`

---

## 🏷️ Tags

`cyber-security` `vulnerability-assessment` `nmap` `owasp-zap` `future-interns` `FUTURE_CS_01`
