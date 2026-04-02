# GitHub issue forms for a hardware product development repo

Put the files in:

```text
.github/ISSUE_TEMPLATE/
```

Included templates:

- Requirement
- Implementation Task
- Verification Test
- Investigation / Experiment
- Bug / Defect
- Component Evaluation
- Change Request
- `config.yml`

## Suggested companion labels

Create these labels in GitHub so the templates classify issues consistently:

### Type labels

- `type: requirement`
- `type: implementation`
- `type: verification`
- `type: investigation`
- `type: bug`
- `type: component-evaluation`
- `type: change-request`

### Optional subsystem labels

- `subsystem: cutting`
- `subsystem: drive`
- `subsystem: power`
- `subsystem: charging`
- `subsystem: pcb`
- `subsystem: firmware`
- `subsystem: sensors`
- `subsystem: logging`
- `subsystem: enclosure`
- `subsystem: lighting`
- `subsystem: mechanical`
- `subsystem: safety`

## Suggested repo workflow

1. Capture needs as **Requirement** issues.
2. Open **Implementation Task** issues that link back to requirements.
3. Use **Verification Test** issues to prove each requirement or fix.
4. Use **Investigation / Experiment** and **Component Evaluation** for R&D and part down-selection.
5. Use **Bug / Defect** for failures and regressions.
6. Use **Change Request** when a baseline requirement or design should change.

## Notes

- The `config.yml` in this package disables blank issues to keep everything structured.
- You can change that by setting `blank_issues_enabled: true`.

