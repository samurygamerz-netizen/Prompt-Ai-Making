# Suggested source repository
```text
ai-computer-platform/
├── README.md
├── docs/{architecture,roadmap,threat-model,decisions}/
├── apps/{control-ui,voice-client}/
├── services/{orchestrator,model-router,tool-broker,host-agent,device-gateway,memory-service,audit-service}/
├── adapters/{llm,stt,tts,devices}/
├── contracts/{tools,devices,events}/
├── configs/{project.example.yaml,device-registry.example.yaml}
├── tests/{unit,integration,security}/
├── deployment/{dev,os-image,recovery}/
├── scripts/
├── data/                 # runtime only; never commit private data
└── .gitignore
```
Keep secrets and runtime user data out of version control. Every tool needs a typed schema, permission tier, timeout and tests.
