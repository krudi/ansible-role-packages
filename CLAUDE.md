# Ansible Role — Packages

Ansible role that installs predefined sets of system packages via the OS package manager.

@AGENTS.md

## For Claude Code

### Rules loaded automatically

| Rule file | Applied to |
|-----------|---|
| `.ai/rules/ansible.md` | `**/*.yml`, `**/*.yaml` |

### Constraints

- Package list comes from `defaults/main.yml` — never hardcode package names in tasks
- Check platform conditionals before adding packages — this role supports Debian/Ubuntu and RHEL/Fedora
- Test idempotency: running the role twice must produce no changes on the second run
