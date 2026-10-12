# Operations and Backup

Health checks: OS/service status, CPU/RAM/disk, model endpoint, STT/TTS, device connectivity, stuck tasks, failed/denied actions and log space.

Back up: configuration excluding secrets, user-approved memory, project files, device metadata without private keys, OS build recipe and recovery instructions. Keep one separate/offline copy, encrypt private backups and test restore.

Incident response: stop new actions; isolate affected device; revoke compromised identity; inspect audit log; restore known-good state; rotate secrets; document root cause.
