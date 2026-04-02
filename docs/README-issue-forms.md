# GitHub issue forms for the mini lawnmower repo

## Folder structure

Place these files in your repository exactly like this:

```text
.github/
└── ISSUE_TEMPLATE/
    ├── config.yml
    ├── 01-requirement.yml
    ├── 02-implementation-task.yml
    ├── 03-verification-test.yml
    ├── 04-investigation-experiment.yml
    ├── 05-bug-defect.yml
    ├── 06-component-evaluation.yml
    └── 07-change-request.yml
```

## Recommended labels

Create these labels in GitHub before you start using the forms:

- requirement
- implementation-task
- verification-test
- investigation-experiment
- bug
- component-evaluation
- change-request

## Notes

- The filenames are prefixed with numbers so GitHub shows them in a useful order.
- `blank_issues_enabled: false` forces contributors to choose a structured form, while maintainers can still open a blank issue if needed.
- The forms intentionally do **not** use the newer top-level `type:` field, because issue types are managed at organization level and are less portable for a personal-account repository.
- You can still use a GitHub Project for Kanban and add these issues to that project manually or with automations.

## Suggested usage flow

1. Create or refine a **Requirement**.
2. Run **Investigation / Experiment** or **Component Evaluation** issues if something is still unknown.
3. Open a **Change Request** if an approved baseline must change.
4. Create one or more **Implementation Task** issues from the approved baseline.
5. Create **Verification Test** issues that verify the requirement or implementation.
6. Use **Bug / Defect** when observed behavior violates the intended behavior or requirement.

## Example traceability chain

```text
Requirement #12
  ├── Component Evaluation #18
  ├── Investigation / Experiment #21
  ├── Change Request #27
  ├── Implementation Task #33
  └── Verification Test #41
```
