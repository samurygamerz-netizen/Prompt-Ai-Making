# AI Core Design

## Modules
Input adapter → intent/task parser → bounded planner → model router → policy engine → typed tool broker → state manager → result verifier → response renderer. Memory is separate and user-controlled.

## Agent loop
1. Receive task.
2. Create bounded plan with step/time/resource limits.
3. Select model only if needed.
4. Validate each tool call independently.
5. Execute one step.
6. Observe actual result and verify it.
7. Update state; continue only when allowed.
8. Stop on failure, limit or cancellation.
9. Report completed and incomplete work honestly.

## Routing inputs
Task type, tested capability, language quality, context size, privacy class, network availability, latency, cost and provider health.

## Tool contracts
Every tool has a name, typed input/output schema, permission tier, timeout and audit requirements. Reject unknown fields. Never execute arbitrary LLM-generated shell text. Limit runtime/output and filesystem scope.

## Memory
Separate task state, approved preferences, project notes and audit records. Provide inspect/edit/delete/export. Never store passwords or API keys in memory.
