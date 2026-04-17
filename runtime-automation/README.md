# runtime-automation

This directory is mounted into the `ansible-runner-api` (zt-runner) container at `/runtime-automation`.

It provides the Ansible Runner project structure used by the zt-runner API to execute automation on behalf of the lab.

## Structure

```
runtime-automation/
├── project/          # Ansible playbooks executed by zt-runner
│   └── *.yml
└── inventory/        # Inventory files (generated at deploy time)
    └── hosts
```

## Note

The `inventory/hosts` file is populated at provisioning time by AgnosticD with the actual lab host details.
The playbooks in `project/` are stubs — replace them with real automation as the lab content evolves.
