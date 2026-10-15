# 🦉 OMinioX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OMinioX** — Self-Hosted S3 Storage Security Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline MinIO / Ceph RGW configuration & S3 bucket-policy auditor

---

## ✨ Features

- MinIO env / config.env auditor — default root credentials, weak & short secrets (always masked), console exposure, plaintext server URL, TLS certs, KMS / SSE, audit & logger webhooks, OpenID / LDAP trust, Prometheus auth, compression of encrypted data
- systemd unit review (root service, missing sandboxing)
- `mc admin` JSON export analysis — users, groups, policies, service accounts, anonymous bucket access
- Ceph RGW ceph.conf auditor — rgw_enable_apis, SSL frontends, Keystone/LDAP trust, SSE keys, cephx
- S3 bucket-policy / IAM policy semantic evaluator — Principal '*', NotPrincipal/NotAction pitfalls, SecureTransport, IpAddress 0.0.0.0/0, Referer trust
- Bucket hygiene — versioning, object-lock, lifecycle, default encryption, CORS wildcard origins
- Effective-access simulator (explicit deny → allow → implicit deny) with condition context
- CWE + MITRE ATT&CK mapping, score & grade
- Exports TXT / MD / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMinioX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
