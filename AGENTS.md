# Ansible Role — Packages

Ansible role that installs predefined sets of system packages via the OS package manager.

## Stack

- Ansible / YAML

## Commands

```bash
ansible-lint       # lint the role
molecule test      # full test (if molecule configured)
```

## Onboarding

**Prerequisites:** Ansible, molecule.

1. `ansible-lint` — verify linting passes
2. `molecule converge` — apply the role
3. `molecule test` — full test including idempotency

---

## Testing

- Run before every PR: `ansible-lint && molecule test`
- Test on both Debian/Ubuntu and RHEL/Fedora if the change affects OS-specific tasks

---

## Notes

- Package list is controlled by variables — see `defaults/main.yml` for the full list
- Supports multiple OS families (Debian/Ubuntu, RHEL/Fedora) — check platform conditionals before adding packages

---

## Rules

@.ai/rules/ansible.md

---

## For Claude Code

### Rules loaded automatically

| Rule file | Applied to |
|-----------|---|
| `.ai/rules/ansible.md` | `**/*.yml`, `**/*.yaml` |

### Constraints

- Package list comes from `defaults/main.yml` — never hardcode package names in tasks
- Check platform conditionals before adding packages — this role supports Debian/Ubuntu and RHEL/Fedora
- Test idempotency: running the role twice must produce no changes on the second run
