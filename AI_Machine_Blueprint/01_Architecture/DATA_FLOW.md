# Data Flow

## Voice path
Microphone → speech recognition → transcript preview → orchestrator → plan → policy check → tool broker → execution → independent verification → text/TTS response.

## Device path
Request → capability lookup → permission check → authenticated gateway → enrolled device API/agent → acknowledgement → verification → audit log.

## Data classes
- Public: generic documentation.
- Personal: preferences and approved memory.
- Private: files, filenames, home network inventory.
- Secret: passwords, API keys, session cookies, private keys.

Secrets belong in an OS credential store or secret manager, never in prompts, logs, repository files or ZIP archives.

## Failure handling
- Low-confidence transcript: ask user to repeat/confirm.
- Provider timeout: bounded retry, then configured fallback or clear failure.
- Permission denied: do not escalate automatically.
- Device offline: report unavailable, never claim success.
- Verification mismatch: stop dependent steps and report uncertainty.
- Cancellation: stop starting new actions and cancel safe-to-cancel work.
