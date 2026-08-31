<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=28&duration=3500&pause=500&color=E37E00&center=true&vCenter=true&width=620&lines=Hi+%F0%9F%91%8B+I'm+Li+Jinquan+%28%E6%9D%8E%E9%87%91%E6%B3%89%29;Security+%2B+AI+%2B+Rust+%2B+Fullstack;Offensive%2C+defensive+and+AI-native+engineering">
</p>

<h1 align="center">Hi 👋, I'm Li Jinquan (李金泉)</h1>
<h3 align="center">Security Engineer · AI-native Builder · 10+ yrs in software engineering</h3>

---

## 🛡️ About Me

Offensive-security-minded engineer who builds and breaks systems for a living — then ships the fixes.

- 🕵️ **Bug bounty hunter** — reported **high/critical** vulnerabilities on **HackerOne** and **Immunefi** (Web3 / smart-contract security), verified by international platforms.
- 🎖️ **CISP** (Certified Information Security Professional).
- 🦀 **Rust deep-diver** — using Rust since its 1.0 era; strong on ownership, borrowing, `unsafe`, FFI, and system-level security.
- 🤖 **AI-native** — private LLM deployment, AI coding assistants, RAG-based customer service, DevSecOps.
- 🏗️ **10+ years** engineering experience since 2016: chip test systems, security tools, microservices architecture.
- 🌱 Currently building an **AI Security** venture — guardrails, red-team automation, and secure AI products.
- 💬 Ask me about: **Rust · Web3 security · AI security · DevSecOps · Reverse engineering**

---

## 🚀 Recent Open-Source Contribution

[![RustSec PR](https://img.shields.io/badge/RustSec-PR%20%231686-4C9F38?style=flat-square&logo=rust&logoColor=white)](https://github.com/RustSec/rustsec/pull/1686)

**Fixed a panic vulnerability in RustSec/cargo-audit** — the de-facto dependency-security auditor for the Rust ecosystem:

- Found & fixed an input-validation crash in `rustsec_refs_imported()` (#1681): malformed OSV reference URLs caused a **panic / DoS vector** for downstream `cargo-audit` / `cargo-deny` users.
- Replaced a hard-coded byte-slice + `.expect()` with `strip_prefix()` + `filter_map()` — malformed URLs are now safely skipped instead of crashing.
- Added unit tests covering valid, truncated, malformed, and mixed reference URLs.
- Patch: single file, **+79 / −5**, no behavioural change for valid input.

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
![Immunefi](https://img.shields.io/badge/Immunefi-CC66FF?style=flat-square&logo=web3&logoColor=white)
![CISP](https://img.shields.io/badge/CISP-Certified-4C9F38?style=flat-square)

**AI / Backend / Frontend**
![LLM](https://img.shields.io/badge/LLM-Private%20Deploy-412991?style=flat-square&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-Search-FF6F00?style=flat-square)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Vue](https://img.shields.io/badge/Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

---

## 🧠 What I'm Building

> **An AI Security venture** — "Guardrails, red-team automation, and secure-by-design AI products."

My angle: I think like an attacker (white-hat), and I build like an engineer. The combination is what AI security actually needs.

---

## 📈 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=li-jin-quan&show_icons=true&theme=default&hide_border=true" height="170" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=li-jin-quan&layout=compact&hide_border=true" height="170" />
</p>

---

<p align="center">
  <i>Security isn't a feature — it's a mindset.</i>
</p>
