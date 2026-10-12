# Open Decisions

1. Total hardware budget in INR?
2. Current PC CPU model?
3. Installed RAM?
4. Storage and GPU?
5. Must main system work offline, sometimes offline, or cloud is acceptable?
6. Which devices should it control (Windows PCs, Android, lights, sensors, etc.)?
7. How many devices?
8. Is local LLM inference mandatory in version 1?
9. Is Linux-based OS acceptable for version 1?
10. Can wake-word wait until push-to-talk works?

Recommended defaults: prototype on current hardware, hybrid mode, Linux-based image, push-to-talk, read-only tools first, device enrollment, no arbitrary shell, confirmation for destructive/privileged actions.

| Risk | Impact | Mitigation |
|---|---|---|
| Buying before benchmarking | Wasted budget | Measure workload first |
| Model exceeds RAM | Slow/crash | Smaller quantized model or cloud route |
| Unsafe tool action | Data loss | Broker, allowlist, confirmation |
| Device compromise | Home network risk | Authentication, segmentation, revocation |
| Cloud privacy exposure | Data leakage | Minimize context and require consent |
| Broken update | Downtime | Rollback and recovery media |
