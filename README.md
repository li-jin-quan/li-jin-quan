<h1 align="center">👋 Hi, I'm Li Jinquan (李金泉)</h1>
<h3 align="center">🛡️ Security Engineer · 🤖 AI-native Builder · 🦀 Rust · 10+ yrs in software engineering</h3>

<p align="center">
  <a href="https://github.com/li-jin-quan"><img src="https://img.shields.io/badge/GitHub-li--jin--quan-181717?style=flat-square&logo=github&logoColor=white"></a>
  <a href="https://hackerone.com"><img src="https://img.shields.io/badge/Bug%20Bounty-HackerOne-494649?style=flat-square&logo=hackerone&logoColor=white"></a>
  <a href="https://immunefi.com"><img src="https://img.shields.io/badge/Immunefi-Web3%20Security-CC66FF?style=flat-square&logo=web3.js&logoColor=white"></a>
  <img src="https://img.shields.io/badge/CISP-Certified%20Info%20Security%20Professional-4C9F38?style=flat-square">
</p>

---

## 🛡️ About Me

Offensive-security-minded engineer who builds and breaks systems for a living — then ships the fixes.

- 🕵️ **Bug bounty hunter** — reported **high / critical** vulnerabilities on **HackerOne** and **Immunefi** (Web3 / smart-contract security), verified on international platforms.
- 🎖️ **CISP** — Certified Information Security Professional.
- 🦀 **Rust deep-diver** — using Rust since the 1.0 era; strong on ownership, borrowing, `unsafe`, FFI, and system-level security.
- 🤖 **AI-native** — private LLM deployment, AI coding assistants, RAG-based customer service, DevSecOps.
- 🏗️ **10+ years** experience since 2016: chip test systems, security tooling, microservices architecture.
- 🌱 Building an **AI Security** venture — guardrails, red-team automation, secure-by-design AI products.
- 💬 Ask me about **Rust · Web3 security · AI security · DevSecOps · Reverse engineering**.

---

## 🚀 Open-Source Contribution

[![RustSec PR #1686](https://img.shields.io/badge/RustSec%2Fcargo--audit-PR%20%231686-4C9F38?style=flat-square&logo=rust&logoColor=white)](https://github.com/RustSec/rustsec/pull/1686)

**Fixed a panic / DoS vulnerability in RustSec / cargo-audit** — the de-facto dependency-security auditor of the Rust ecosystem.

- Found & fixed an input-validation crash in `rustsec_refs_imported()` ([#1681](https://github.com/RustSec/rustsec/issues/1681)): malformed OSV reference URLs caused a **panic**, crashing `cargo-audit` / `cargo-deny` for downstream users.
- Replaced a hard-coded byte-slice + `.expect()` with `strip_prefix()` + `filter_map()` — malformed URLs are now safely skipped instead of crashing.
- Added unit tests covering valid, truncated, malformed, and mixed reference URLs.
- Single-file patch, **+79 / −5**, zero behavioural change for valid input.

---

## 🛠️ Tech Stack

**Languages**
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)

**Security**
![HackerOne](https://img.shields.io/badge/HackerOne-494649?style=flat-square&logo=hackerone&logoColor=white)
![Immunefi](https://img.shields.io/badge/Immunefi-CC66FF?style=flat-square&logo=web3.js&logoColor=white)
![CISP](https://img.shields.io/badge/CISP-Certified-4C9F38?style=flat-square)

**AI / Backend / Frontend**
![LLM](https://img.shields.io/badge/LLM-Private%20Deploy-412991?style=flat-square&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-Customer%20Service-FF6F00?style=flat-square)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Vue](https://img.shields.io/badge/Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

---

## 🧠 Building

> **An AI Security venture** — *guardrails, red-team automation, and secure-by-design AI products.*

I think like an attacker (white-hat) and build like an engineer — the combination AI security actually needs.

---

<p align="center">
  <i>Security isn't a feature — it's a mindset.</i>
</p>
