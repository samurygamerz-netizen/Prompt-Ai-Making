# Hardware and OS Plan

## Hardware criteria
Select only after workload/budget: CPU support, RAM headroom, SSD capacity/endurance, optional GPU/NPU, Ethernet/Wi-Fi, microphone/speakers, power/cooling, upgradeability and recovery media.

Model file size is not total RAM usage: runtime also needs KV cache, context, libraries and OS memory. Quantization lowers memory use but can affect quality. Benchmark the actual model on the actual machine before purchase.

## OS strategy
Version 1 should be a custom Linux-based image, not a new kernel. Keep the AI service unprivileged; put host control behind a narrow separate agent. Enable firewall, minimize services, use reproducible configuration, integrity-checked updates, rollback and bootable recovery.

## Kernel strategy
A new kernel entails boot support, memory management, scheduling, drivers, storage/network stacks, security boundaries and debugging. Study it separately after a working system exists.

## Custom electronics later
Use microcontroller/SBC prototypes for sensors and I/O. Define electrical limits and safe defaults. A device must fail to a safe state if network or AI fails. Never let LLM output directly control safety-critical actuators.

## Required before buying hardware
- Budget in INR.
- Current CPU/RAM/storage/GPU.
- Local LLM required or cloud acceptable.
- Number/type of devices.
- Always-on and power-use expectations.
