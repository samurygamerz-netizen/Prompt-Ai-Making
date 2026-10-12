# Personal AI Computer Platform — Blueprint Pack

यह पैकेज architecture, roadmap, hardware/OS strategy, AI core, device access, data schemas, testing और decisions को अलग-अलग फाइलों में रखता है। यह **design blueprint** है, तैयार OS या पूरा उत्पाद नहीं।

## सही शुरुआती दिशा
- पहले मौजूदा PC पर prototype; शुरुआत में नया kernel या CPU नहीं।
- Hybrid architecture: जरूरत के अनुसार cloud LLM और वैकल्पिक local model।
- AI planner और privileged host-control agent अलग रखें।
- पहले read-only status tools, फिर sandboxed/reversible actions।
- केवल अपने/अनुमति प्राप्त devices enroll करें; destructive/privileged actions पर confirmation।

## Folder guide
- `01_Architecture/`: system diagram, data flow, repository structure.
- `02_Roadmap/`: implementation phases, milestones.
- `03_Hardware_OS/`: hardware selection, custom Linux OS and recovery.
- `04_AI_Core/`: orchestration, model routing, voice and memory.
- `05_Device_Network_Security/`: device enrollment, threat model.
- `06_Data_Schemas/`: example configuration and tool/device contracts.
- `07_Operations_Testing/`: testing, backup and operations.
- `08_Decisions/`: unanswered decisions and risks.
- `PROJECT_PLAN.csv`: task tracker.
- `SOURCES_AND_RESEARCH.md`: official documentation reviewed for this plan.

## Read first
1. `01_Architecture/SYSTEM_ARCHITECTURE.md`
2. `02_Roadmap/IMPLEMENTATION_ROADMAP.md`
3. `03_Hardware_OS/HARDWARE_AND_OS_PLAN.md`
4. `04_AI_Core/AI_CORE_DESIGN.md`
5. `05_Device_Network_Security/SECURITY_AND_DEVICE_ACCESS.md`
6. `08_Decisions/OPEN_DECISIONS.md`
