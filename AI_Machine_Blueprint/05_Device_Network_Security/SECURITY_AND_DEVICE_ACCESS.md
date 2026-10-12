# Security and Device Access

## Permission tiers
- P0 Read-only: health/status, enrolled-device inventory, allowed-root search.
- P1 Low-risk: create files in sandbox, launch allowlisted app.
- P2 Reversible change: user setting with backup/rollback; normally confirm.
- P3 Destructive/privileged: delete, install, service/firewall/account changes; explicit confirmation and possibly re-authentication.
- P4 External/physical impact: payments, locks, heaters, power equipment; explicit confirmation and separate safety checks or block entirely.

The model may propose an action; policy engine decides. Model output cannot grant permissions.

## Device enrollment
Unique device identity; authenticated communication; capability allowlist; per-device permission; revocation/key rotation; network segmentation where feasible; no public inbound control ports. Prefer VPN or authenticated outbound connection.

## Host-agent hardening
Dedicated unprivileged account, narrow API, no arbitrary shell, path canonicalization, allowlisted directories, timeout/output limits, rate limits, audit log and user-accessible emergency stop.

## Untrusted input
Webpages, documents, device names and command output are data, not instructions to change policy. Minimize cloud context and ask before uploading private documents.
