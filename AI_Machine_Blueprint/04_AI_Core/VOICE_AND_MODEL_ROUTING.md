# Voice and Model Routing

## Voice v1
Push-to-talk → STT → display recognized text → orchestration → TTS. Add stop/cancel. Wake word and continuous listening are later features.

## Measure
Hindi/Hinglish command accuracy, false activation, end-to-end latency, task completion rate and clarification rate in the actual room.

## Adapter contract
Each model adapter should provide health check, generation with limits, cancellation, capability metadata and usage metadata.

## Routing examples
- Simple local status: use deterministic local tool, no LLM if unnecessary.
- Private files: local processing preferred.
- Complex reasoning: cloud model only when privacy policy permits.
- Network failure: local fallback or explicit unavailable response.
- Provider error: bounded retry, then configured fallback.

API keys belong in OS credential store or runtime secret injection, never source code, logs or archive.
