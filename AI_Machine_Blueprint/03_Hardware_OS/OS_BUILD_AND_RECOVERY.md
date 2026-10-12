# OS Build, Update and Recovery

1. Pin base OS and package versions.
2. Keep configuration in version control.
3. Build repeatable image in a clean environment.
4. Run boot/service tests in a VM.
5. Test on target hardware.
6. Integrate integrity checks and signed updates.
7. Keep a known-good image and rollback path.
8. Create bootable recovery media and document restore steps.
9. Test recovery before relying on the system.

Do not start with a new kernel. Package the application on a supported base OS first.
