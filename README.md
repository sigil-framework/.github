<div align="center">

<pre>
     ███████╗██╗ ██████╗ ██╗██╗     
     ██╔════╝██║██╔════╝ ██║██║     
     ███████╗██║██║  ███╗██║██║     
     ╚════██║██║██║   ██║██║██║     
     ███████║██║╚██████╔╝██║███████╗
     ╚══════╝╚═╝ ╚═════╝ ╚═╝╚══════╝
</pre>

### [ SECURE ISOLATION, GUARDRAIL & INTEGRITY LAYER ]
*Infrastructure bound by precision. Zero fluff. Absolute system control.*

`SYS_STATUS: ONLINE` &nbsp;||&nbsp; `ENV: PRODUCTION` &nbsp;||&nbsp; `SEC_LEVEL: STRICT`

</div>

---

## Ecosystem Architecture

The **SiGiL Framework** is a modular ecosystem of security-focused infrastructure, low-level execution engines, and custom system distributions. Built for environments where packet isolation, signal integrity, and absolute operational boundaries are mandatory.

```text
+-------------------------------------------------------------------+
|                        SiGiL ECOSYSTEM                            |
+-------------------+--------------------+--------------------------+
|  SECURITY & PROXY |  AUDITING & THREAT |  OPERATING ENVIRONMENT   |
+-------------------+--------------------+--------------------------+
|  SiGiL-Proxy      |  Sentinel-X        |  Aberration OS           |
|  [Go / Reverse]   |  [Go / eBPF]       |  [Debian / Cobalt]       |
+-------------------+--------------------+--------------------------+
```

---

## Core Pillars

### 1. SiGiL-Proxy
High-performance, commercial-grade Go reverse proxy and guardrail engine. Implements per-IP rate limiting, cryptographic trace ID injection (`X-Sigil-Request-ID`), and real-time packet sanitization for local LLM traffic and sensitive endpoints.

### 2. Sentinel-X
Kernel-level threat monitoring and system audit engine written in Go and eBPF. Monitors system calls, socket bindings, and raw network telemetry in real time with near-zero overhead.

### 3. Aberration OS
Debian-based Linux distribution pre-configured with security tooling, custom window management, and a stark Electric Cobalt visual signature.

---

## System Directives

*   **Zero Dependencies**: Infrastructure tools compile to static binaries. No bloat, no runtime overhead.
*   **Terminal-First**: Built for system engineers, lockstep isolation, and CLI-driven control.
*   **Absolute Boundaries**: If traffic violates routing rules or rate limits, it is dropped at the gate.

---

## Quick Start (SiGiL-Proxy)

### Build Static Binary
```bash
git clone [https://github.com/KadeHood/sigil-framework.git](https://github.com/KadeHood/sigil-framework.git)
cd sigil-framework/proxy
CGO_ENABLED=0 go build -ldflags="-s -w" -o ../bin/sigil-proxy .
```

### Deploy via Docker
```bash
cd deploy
docker compose up -d --build
```

### Route Traffic
```bash
export OPENAI_API_BASE="[http://127.0.0.1:8080/v1](http://127.0.0.1:8080/v1)"
```

---

## Repository Structure

```text
sigil-framework/
├── proxy/        # SiGiL-Proxy Go reverse proxy, rate limiter, and packet sanitizer
├── sentinel/     # Sentinel-X Go + eBPF kernel telemetry probes
├── aberration/   # Aberration OS build configs, SquashFS overlays, and Cobalt dotfiles
├── deploy/       # Dockerfiles, docker-compose.yml, and systemd units
├── config/       # Default routing rules and YAML configurations
└── web/          # Landing page assets for sigil-framework.space
```

---

<div align="center">

**SIGIL-FRAMEWORK // INFRASTRUCTURE BOUND BY PRECISION**

</div>
