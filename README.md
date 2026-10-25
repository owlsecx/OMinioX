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

OMinioX is an offline MinIO / Ceph RGW configuration and S3 bucket-policy auditor. It reviews env/config files, systemd units, `mc admin` JSON exports, Ceph RGW settings, and IAM/bucket policies, including an effective-access simulator. Operation is 100% offline and read-only with CWE/MITRE mapping and multi-format export.

---

## ✨ Features

- MinIO env/config.env audit: default root creds, weak secrets (masked), console exposure, TLS, KMS/SSE, webhooks, OpenID/LDAP, Prometheus auth
- systemd unit review for root service and missing sandboxing
- `mc admin` JSON export analysis: users, groups, policies, service accounts, anonymous bucket access
- Ceph RGW ceph.conf checks: APIs, SSL frontends, Keystone/LDAP trust, SSE keys, cephx
- S3 bucket-policy / IAM semantic evaluator and effective-access simulator with condition context
- Bucket hygiene (versioning, object-lock, lifecycle, encryption, CORS); score/grade; TXT/MD/JSON/CSV/SARIF

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMinioX --env config.env --policy bucket.json --scan
./OMinioX --simulate "*" s3:GetObject "arn:aws:s3:::data/*" --format json -o minio.json
./OMinioX --demo --fail-on high
./OMinioX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
