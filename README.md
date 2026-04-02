# GitHub issue forms for a hardware product repo

This version uses a **2-axis classification** inside every issue form:

1. **Discipline**
   - Mechanical
   - Electronics / power
   - Firmware / software
   - Test / validation
   - Systems / integration
   - Manufacturing / documentation
   - Multi-disciplinary

2. **Assembly / module**
   - Cutting module
   - Drive module
   - Energy module
   - Charging / solar module
   - Control module
   - Sensor module
   - Chassis / enclosure
   - HMI / lighting
   - Logging / telemetry
   - Safety
   - System-wide / cross-cutting

## Why this structure works better

Do **not** make "cutting system" or "drive system" your only top-level categories.
Instead separate:
- **what kind of work item it is** → requirement, task, test, bug, experiment, evaluation, change request
- **which discipline owns it** → mechanical / electronics / firmware / etc.
- **which assembly it belongs to** → cutting, drive, energy, control, etc.

That lets you create issues such as:
- Requirement + Safety + Cutting module
- Implementation Task + Firmware / software + Cutting module
- Implementation Task + Mechanical + Cutting module
- Component Evaluation + Electronics / power + Drive module
- Verification Test + Test / validation + Sensor module

## Recommended linking model in GitHub

Use these relationships consistently:

### 1. Requirement as the parent
Create one requirement issue for the need itself.
Example:
- `[REQ] Cutting module shall stop safely on tip-over`

### 2. Child issues by discipline
Create separate child issues for implementation work in each discipline.
Example children:
- `[TASK] Mechanical guard concept for cutting module`
- `[TASK] Blade motor driver circuit for cutting module`
- `[TASK] Tip-over stop logic in firmware`

### 3. Verification linked back to the requirement
Create one or more test issues that verify the requirement.
Example:
- `[TEST] Verify cutting shutdown time after tip-over`

### 4. Experiments and evaluations feed decisions
Use investigation and component evaluation issues before locking the design.
Link them from the requirement or change request.

### 5. Change requests modify baselines
If a requirement, selected part, or architecture changes later, open a change request and link all affected items.

## Recommended label scheme

Create labels such as:

### Type labels
- `type: requirement`
- `type: implementation`
- `type: verification`
- `type: investigation`
- `type: defect`
- `type: component-evaluation`
- `type: change-request`

### Discipline labels
- `disc: mechanical`
- `disc: electronics`
- `disc: firmware`
- `disc: test`
- `disc: systems`
- `disc: manufacturing`
- `disc: multi`

### Assembly labels
- `asm: cutting`
- `asm: drive`
- `asm: energy`
- `asm: charging`
- `asm: control`
- `asm: sensors`
- `asm: chassis`
- `asm: hmi`
- `asm: logging`
- `asm: safety`
- `asm: system`

## Suggested GitHub Project fields

If you use GitHub Projects, add these fields manually:
- Status
- Discipline
- Assembly
- Priority
- Verification status
- Prototype / revision

## Folder placement

Put the YAML files in:

`.github/ISSUE_TEMPLATE/`
