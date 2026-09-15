<h1 align="center">👋 Hi, I'm Li Jinquan (李金泉)</h1>
<h3 align="center">🛡️ Security Engineer · 🤖 AI-native Builder · 🦀 Rust · 10+ yrs in software engineering</h3>

<p align="center">
  <a href="https://github.com/li-jin-quan"><img src="https://img.shields.io/badge/GitHub-li--jin--quan-181717?style=flat-square&logo=github&logoColor=white"></a>
  <a href="https://github.com/sonos/tract/pulls?q=is%3Apr+author%3Ali-jin-quan+is%3Amerged"><img src="https://img.shields.io/badge/sonos%2Ftract-4%20security%20PRs%20merged-4C9F38?style=flat-square&logo=rust&logoColor=white"></a>
  <img src="https://img.shields.io/badge/Upstream%20Security-19%20PRs%20%C2%B7%206%20merged-blueviolet?style=flat-square">
  <img src="https://img.shields.io/badge/GHSA-reporter%20credit-lightgrey?style=flat-square&logo=github">
</p>

<p align="center">
  📄 <a href="https://github.com/li-jin-quan/resume">View my Resume</a> · <a href="https://li-jin-quan.github.io/resume/">Online Preview</a>
</p>

---

## 🛡️ About Me

Offensive-security-minded engineer who builds and breaks systems for a living — then ships the fixes.

- 🕵️ **Security researcher** — independent audits of the Rust AI/ML supply chain: **19 upstream security PRs** submitted (CWE-770 / CWE-190 / CWE-248 class), of which **6 are merged** — 4 in `sonos/tract`, 1 in `zip-rs/zip2`, 1 in `tracel-ai/burn` — and 11 are under review. Every one is a real code change, not a typo fix — see the list below.
- 🌐 **International bounty experience** — registered researcher on HackerOne (`0xNuoyaArk`) and Immunefi (Web3 / smart-contract security); familiar with report writing and triage workflows end to end.
- 🦀 **Rust deep-diver** — using Rust since 2016; strong on ownership, borrowing, `unsafe`, FFI, and system-level security.
- 🤖 **AI-native** — private LLM deployment, AI coding assistants, RAG-based customer service, DevSecOps.
- 🏗️ **10+ years** experience since 2016: chip test systems, security tooling, microservices architecture.
- 🌱 Building an **AI Security** venture — guardrails, red-team automation, secure-by-design AI products.
- 💬 Ask me about **Rust · Web3 security · AI security · DevSecOps · Reverse engineering**.

---

## 🚀 Open-Source Security Work

### Merged — 6 PRs across 3 repositories

| PR | What it fixes |
|---|---|
| [#2766](https://github.com/sonos/tract/pull/2766) | `Harden read_tensor against untrusted NNEF string lengths` — untrusted length fields drove unchecked allocations (CWE-770) |
| [#2795](https://github.com/sonos/tract/pull/2795) | `fix(data): check tensor shape arithmetic before allocation` — overflow in shape math before the allocation (CWE-190 / CWE-770) |
| [#2796](https://github.com/sonos/tract/pull/2796) | `fix(tensorflow): return errors instead of panicking` — malformed `TensorProto` panicked instead of erroring (CWE-248) |
| [#2814](https://github.com/sonos/tract/pull/2814) | `Add missing sign checks on loader dims casts` (onnx / tflite) — negative dims became huge `usize` after the cast |
| [#984](https://github.com/zip-rs/zip2/pull/984) | `zip-rs/zip2` — a symlink entry with a huge **declared** size drove `with_capacity` before a single byte was read (CWE-770). Merged through GitHub's merge queue on 2026-09-14; **not in a release yet** |
| [#5667](https://github.com/tracel-ai/burn/pull/5667) | `tracel-ai/burn` — a sparse file reported a 3.4 TB size, bypassing the metadata-based length check and driving a multi-TB allocation in the MNIST reader; item counts are now capped at the split size (CWE-770). Merged 2026-09-14; **not in a release yet** |

**GHSA-6ffw-f7m6-gpxj** — I'm credited as the reporter. The advisory is currently in **draft**
upstream (CVE requested, not yet assigned); draft advisories aren't public, so the GHSA link
will 404 until the maintainers publish it.

<details>
<summary><b>Under review — 11 PRs across the Rust AI/ML ecosystem</b> (click to expand)</summary>

| Repo | PR | What it fixes | Size |
|---|---|---|---|
| huggingface/candle | [#3970](https://github.com/huggingface/candle/pull/3970) | ggml: unbounded allocations from untrusted values | +126 |
| huggingface/candle | [#3962](https://github.com/huggingface/candle/pull/3962) | npy: unbounded allocation when reading arrays | +38 |
| huggingface/candle | [#3961](https://github.com/huggingface/candle/pull/3961) | pickle: unbounded allocation in binary protocol | +53 |
| huggingface/hf-hub | [#202](https://github.com/huggingface/hf-hub/pull/202) | `download_file_to_bytes` trusts untrusted length | +106 |
| daac-tools/vibrato | [#167](https://github.com/daac-tools/vibrato/pull/167) | dictionary: connection matrix allocation | +66 |
| not-fl3/nanoserde | [#172](https://github.com/not-fl3/nanoserde/pull/172) | `DeBin` vs untrusted length prefixes | +110 |
| finalfusion/finalfusion-rust | [#203](https://github.com/finalfusion/finalfusion-rust/pull/203) | format readers vs untrusted length prefixes | +272 |
| ExpHP/npyz | [#84](https://github.com/ExpHP/npyz/pull/84) | `read_header` vs untrusted `header_size` | +16 |
| zurawiki/tiktoken-rs | [#166](https://github.com/zurawiki/tiktoken-rs/pull/166) | `_decode_native_and_split` out-of-bounds | +62 |
| jturner314/ndarray-npy | [#106](https://github.com/jturner314/ndarray-npy/pull/106) | bound allocations by data actually present | +262 |
| KeeperHub/agentic-wallet | [#40](https://github.com/KeeperHub/agentic-wallet/pull/40) | *feature work (MCP pre-execution tool), not a security fix* | +4827 |

These are all awaiting maintainer review — none has been merged yet.

</details>

### RustSec / cargo-audit — found independently, closed as duplicate

I found a panic in `rustsec_refs_imported()`: malformed OSV reference URLs hit a hard-coded
byte-slice plus `.expect()`, crashing `cargo-audit` / `cargo-deny` for downstream users.
My fix ([#1686](https://github.com/RustSec/rustsec/pull/1686)) replaced it with
`strip_prefix()` + `filter_map()` and added unit tests (+79 / −5, no behaviour change for
valid input).

A community fix ([#1683](https://github.com/RustSec/rustsec/pull/1683)) had already been filed,
so mine was **closed as a duplicate — it was never merged**. #1683 is still open upstream, so
the bug itself remains unfixed today.

Listed for the record. The merged work is the PRs listed above.

---

## 🧩 Reverse Engineering

[`crackmes-writeups`](https://github.com/li-jin-quan/crackmes-writeups) — crackmes.one
challenges (Windows x86-64 Rust binaries) solved by **static analysis** with `pefile` +
`capstone`.

- 1 ✅ solved · 1 ✅ proven unsolvable-as-shipped (AES-256-GCM container fully recovered and
  documented) · 1 ⏳ in progress

I publish the unsolved one on purpose. A portfolio that only shows wins is not a portfolio,
it's marketing.

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
![tract](https://img.shields.io/badge/sonos%2Ftract-4%20merged-4C9F38?style=flat-square&logo=rust&logoColor=white)
![zip2](https://img.shields.io/badge/zip-rs%2Fzip2-1%20merged-4C9F38?style=flat-square&logo=rust&logoColor=white)
![burn](https://img.shields.io/badge/tracel--ai%2Fburn-1%20merged-4C9F38?style=flat-square&logo=rust&logoColor=white)
![GHSA](https://img.shields.io/badge/GHSA-reporter-lightgrey?style=flat-square&logo=github)
![OWASP](https://img.shields.io/badge/OWASP-Top%2010-000000?style=flat-square)
![Web3](https://img.shields.io/badge/Web3-Smart%20Contract%20Audit-F16822?style=flat-square&logo=ethereum&logoColor=white)
![DevSecOps](https://img.shields.io/badge/DevSecOps-CI%2FCD%20Integrated-FF6F00?style=flat-square)

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
