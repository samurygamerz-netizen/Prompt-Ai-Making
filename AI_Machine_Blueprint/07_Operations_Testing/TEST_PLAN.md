# Test Plan

## Unit tests
- Unknown tools/fields rejected.
- Permission policy denies unlisted actions.
- Path traversal outside allowed roots blocked.
- Secrets redacted.
- Cancellation prevents later steps.
- Router handles timeout/provider failure.

## Integration tests
- STT transcript reaches orchestrator.
- Orchestrator calls broker, not shell directly.
- Results verified before final response.
- Unenrolled device rejected; revoked device loses access.
- Private documents not sent to cloud by default.
- Failed update rolls back.

## Security tests
Prompt injection cannot change policy; invalid arguments rejected; rate limiting works; logs have no credentials; host agent cannot access outside roots; control APIs are not public.

## Performance tests
Idle CPU/RAM, STT accuracy/latency, LLM response latency, tool latency, crash recovery, power and thermals.

A task is not successful solely because the model says it is; require tool/device evidence.
