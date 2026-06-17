<p align="center">
  <img src="./assets/uffs-hero-1024.png" alt="Sky, LLC — UFFS hero mark" width="360">
</p>

<h1 align="center">Sky, LLC</h1>

<p align="center">
  <b>High-performance systems engineering in Rust.</b><br>
  Makers of <a href="https://github.com/skyllc-ai/UltraFastFileSearch">UltraFastFileSearch</a> — wire-speed NTFS file search.<br>
  Open source core. Commercial GUI/TUI in development.
</p>

<p align="center">
  <a href="https://github.com/skyllc-ai/UltraFastFileSearch/actions/workflows/pr-fast.yml"><img src="https://img.shields.io/github/actions/workflow/status/skyllc-ai/UltraFastFileSearch/pr-fast.yml?branch=main&label=CI" alt="UFFS CI"></a>
  <a href="https://github.com/skyllc-ai/UltraFastFileSearch/releases/latest"><img src="https://img.shields.io/github/v/release/skyllc-ai/UltraFastFileSearch?label=UFFS%20release" alt="UFFS release"></a>
  <a href="https://github.com/skyllc-ai/UltraFastFileSearch/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MPL--2.0-brightgreen.svg" alt="License: MPL-2.0"></a>
  <a href="https://github.com/skyllc-ai/UltraFastFileSearch/issues"><img src="https://img.shields.io/github/issues/skyllc-ai/UltraFastFileSearch?label=open%20issues" alt="Open issues"></a>
  <a href="https://github.com/skyllc-ai/UltraFastFileSearch/blob/main/TRADEMARK.md"><img src="https://img.shields.io/badge/brand-TRADEMARK.md-ce422b.svg" alt="Brand policy"></a>
</p>

---

## What we ship

### UltraFastFileSearch (UFFS)

A Rust-native file search engine that parses the NTFS Master File Table
directly and answers queries in the single-digit millisecond range, even
against tens of millions of records.

**Numbers** (v0.5.66, measured, 7 NTFS drives, ~26 M records):

- 26 M records → CSV in **13.6 s** (1.72 M records/sec sustained)
- Hot daemon query p50: **sub-millisecond** on common patterns
- **~16× faster** than the equivalent C++ reference on hot queries
- Linear memory: **~181 MB per million records**

Open source under MPL-2.0. One engine, one daemon, one CLI, one TUI, one
Python/Polars facade — all sharing the same MFT core.

- Repo: [**skyllc-ai/UltraFastFileSearch**](https://github.com/skyllc-ai/UltraFastFileSearch)
- [Benchmarks →](https://github.com/skyllc-ai/UltraFastFileSearch/tree/main/docs/benchmarks)
- [Methodology →](https://github.com/skyllc-ai/UltraFastFileSearch/blob/main/docs/benchmarks/methodology.md)
- [User manual →](https://github.com/skyllc-ai/UltraFastFileSearch/tree/main/docs/user-manual)

### UFFS Commercial Frontends — in development

A polished GUI and monetized TUI built on top of the open-source UFFS
engine. Target users: developers, sysadmins, and incident responders who
search millions of files daily and need something elegant *and* stupid-fast.

**Interested?** Email [`partnerships@uffs.io`](mailto:partnerships@uffs.io) or open a
[GitHub discussion](https://github.com/skyllc-ai/UltraFastFileSearch/discussions)
with the `commercial-interest` label.

---

## For recruiters and collaborators

This organization is the public engineering portfolio of **Robert Nio**.
The code under [`skyllc-ai/*`](https://github.com/skyllc-ai) is the work sample.

### Stack

- **Rust** (2024 edition, async Tokio, `unsafe` where it earns the perf)
- **NTFS MFT** direct parsing, zero-copy record reads
- **SIMD trigram indexing** for substring search over tens of millions of records
- **Multi-drive parallelism** via a daemon + thin-client split
- **Cross-platform**: Windows (primary target), macOS (dev/offline analysis), Linux (daemon)

### Engineering discipline (all publicly verifiable in the repo)

- Branch-protected `main`, PR-based workflow, signed commits (GPG, GitHub-verified)
- Nextest CI, REUSE/SPDX-compliant licensing, deny-unwrap workspace lints
- Reproducible benchmarks with published methodology and raw capture logs
- Architecture docs + user manual shipped with the code
- Conventional commits, semantic versioning

### Contact

- Engineering roles / technical collaboration: [`careers@uffs.io`](mailto:careers@uffs.io)
- PGP signing key: `E406D32B4736D09F` (ed25519, published on the GitHub profile)

---

## Support the work

Formal sponsor channels (GitHub Sponsors, Ko-fi) are in application/setup.
Until those go live, the most useful things you can do:

- Star the [UFFS repo](https://github.com/skyllc-ai/UltraFastFileSearch)
- Open an issue or file a PR — real-world use cases shape the roadmap
- Share the repo with someone who cares about fast tools

---

<p align="center">
  <sub>© 2025–2026 Sky, LLC. · Built for people who think milliseconds matter.</sub>
</p>
