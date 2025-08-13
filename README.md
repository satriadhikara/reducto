# Reducto

**Reducto** is a high-performance, distributed build cache designed to **cut CI build times by 30–80%** through deterministic, content-addressable artifact storage and cross-job/branch reuse.

> Think of it as a *language-agnostic, S3-backed, build artifact cache* with adapters for your favorite tools and CI systems.

---

## 🚀 Goals

- **Speed up builds** by reusing outputs across jobs, branches, and CI runs.
- **Be language/tool agnostic** via adapters for Node, Rust, Docker, Java, Python, Go, and more.
- **Integrate easily** with GitHub Actions, GitLab, Jenkins, and other CI platforms.
- **Be cloud-portable** — works with S3, MinIO, GCS, Azure Blob, or local disk.

---

## 🔑 Core Concepts

- **Cache Key** — Deterministic hash of all build inputs:  
  `SHA256(build_tool_version, os/arch, env_matrix, dependency_lock, source_fingerprints, build_flags, secrets_salt)`
- **Artifact Manifest** — JSON metadata describing produced files, digests, sizes, and related tool metadata.
- **CAS Objects** — Stored by digest (SHA256), optionally zstd-compressed and split into 4–32 MiB chunks for resumable I/O.

---

## 📌 Status

**Early development** — no code yet.  
<!-- Follow along in [Issues](../../issues) and [Discussions](../../discussions) for design updates. -->

---
