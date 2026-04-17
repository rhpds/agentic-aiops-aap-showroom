# runtime-automation

This directory is mounted into the `ansible-runner-api` (zt-runner) container
at `/runtime-automation` and provides per-module solve and validation playbooks.

## Structure

```
runtime-automation/
├── module-00/
│   ├── solve.yml       # Solve steps for module 00
│   └── validation.yml  # Validation checks for module 00
├── module-01/
│   ├── solve.yml
│   └── validation.yml
└── ...
```

## Plugins

- `validation_check` — conditional check, writes pass/fail message
- `lab_check_fail` — writes error and fails the playbook

These are provided by the zt-runner container image.
