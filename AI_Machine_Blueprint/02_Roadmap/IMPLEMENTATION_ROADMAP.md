# Implementation Roadmap

## Phase 0 — Requirements
Record INR budget, current CPU/RAM/storage/GPU, device list, online/offline needs, privacy and response-time targets. Do not buy hardware before requirements and benchmarks.

## Phase 1 — Text-first prototype
Build a small UI, one model adapter, task state, read-only system status, allowlisted file search, tool broker and logs. Exit: unknown tools/arguments are rejected; tool results are verified.

## Phase 2 — Voice
Add Hindi/Hinglish STT, transcript preview, TTS and push-to-talk. Add wake-word only after basic voice works. Exit: uncertain commands trigger clarification; user can interrupt/cancel.

## Phase 3 — Safe host automation
Add allowlisted app launch and file operations in configured roots. Separate the low-privilege host agent. Exit: no arbitrary shell; destructive/privileged changes require explicit confirmation.

## Phase 4 — Routing and memory
Add local/cloud adapters, privacy-aware routing, fallback, and user-controlled memory. Exit: memory can be viewed/edited/deleted; private files are not sent to cloud by default.

## Phase 5 — Device gateway
Enroll devices with unique identity, authentication, per-device capabilities and revocation. Prefer segmented network/VPN; never expose control APIs to public internet. Exit: unenrolled/revoked devices are denied.

## Phase 6 — Custom OS image
Start from a supported Linux distribution; package services, harden defaults, create reproducible build, integrity-checked updates, rollback and recovery. Test in VM then target hardware.

## Phase 7 — Dedicated hardware
Benchmark workload first. Select CPU/RAM/SSD/network/audio; add GPU/NPU only when justified. Test power, cooling and local-model latency.

## Phase 8 — Custom electronics (optional)
Prototype sensor/IO board or microcontroller only for defined needs. Keep safety-critical logic independent of the LLM. FPGA/ASIC/CPU design is a separate long-term research effort.

## Phase 9 — Reliability
Automate unit, integration and security tests; verify backups and restore; add health checks, installer, logs and operator guide.

**Order matters:** prove AI + tools + device permissions on existing hardware before custom kernel/CPU work.
