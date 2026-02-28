# VulnVault 🔐

**VulnVault** is a practical, developer‑first knowledge base of common and critical application security vulnerabilities, covering the full lifecycle from **code** to **build**, **infrastructure**, and **deployment**.

It provides **clear explanations**, **realistic insecure vs secure code examples**, and **actionable guidance** across **multiple programming languages and frameworks** to help teams build secure applications by default.

> 🎯 Goal: Uplift the organisation’s application security posture by making secure coding **understandable, accessible, and repeatable**.

---

## Why VulnVault?

Most security guidance is either:
- Too abstract to apply, or  
- Too security‑centric to resonate with developers  

VulnVault bridges that gap by:
- Showing **what insecure code actually looks like**
- Explaining **why it’s vulnerable**
- Demonstrating **how to fix it properly**
- Mapping issues to **real‑world impact and controls**

This repo is designed to be used by:
- Developers  
- Tech leads & architects  
- AppSec & DevSecOps teams  
- Engineering onboarding programs  

---

## What’s Inside

VulnVault is organised by **vulnerability category**, not by tool or standard.

Each vulnerability typically includes:

- ✅ **Description & Risk**
- ✅ **How the vulnerability occurs**
- ✅ **Insecure code examples**
- ✅ **Secure code examples**
- ✅ **Language / framework‑specific nuances**
- ✅ **Prevention & best practices**
- ✅ **Related standards** (OWASP Top 10, CWE, ASVS)

---

## Vulnerability Coverage (Examples)

- Injection (SQL, NoSQL, OS Command)
- Cross‑Site Scripting (XSS)
- Cross‑Site Request Forgery (CSRF)
- Authentication & Session Management
- Authorization & Access Control
- Insecure Deserialization
- Security Misconfiguration
- Sensitive Data Exposure
- File Upload & Path Traversal
- Server‑Side Request Forgery (SSRF)
- Dependency & Supply Chain Risks
- Secrets Management
- Cloud & Container Misconfigurations

---

## Supported Languages & Frameworks

Examples are written using **realistic application patterns**, not contrived snippets.

Current coverage includes (and is expanding):

- **Java**
  - Spring / Spring Boot
- **JavaScript / TypeScript**
  - Node.js
  - Express
- **Python**
  - Flask
  - Django
- **C#**
  - ASP.NET / ASP.NET Core
- **Go**
- **Infrastructure & Platform**
  - Docker
  - Kubernetes
  - CI/CD pipelines (generic patterns)

Each example contrasts **❌ insecure** and **✅ secure** implementations side‑by‑side.

---

## Example

### SQL Injection (Java – Spring Boot)

#### ❌ Insecure
```java
String query = "SELECT * FROM users WHERE username = '" + username + "'";
Statement stmt = connection.createStatement();
ResultSet rs = stmt.executeQuery(query);
