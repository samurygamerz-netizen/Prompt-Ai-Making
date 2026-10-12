# Threat Model

Assets: personal files, credentials, OS/admin account, home network, enrolled devices, memory and audit history.

Threats: voice misrecognition, prompt injection, stolen API key, rogue device enrollment, path traversal, overprivileged host agent, compromised device, bad update, network outage.

Mitigations: transcript confirmation for risky tasks; external policy engine; least privilege; typed allowlisted tools; device authentication/revocation; secret manager; integrity-checked updates; logs without secrets; tested backups; manual stop switch; safe default state.

Residual risk remains if the host, update chain or physical device is compromised. Safety-critical controls must not depend on the LLM.
