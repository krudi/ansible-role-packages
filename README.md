# ansible-role-packages

A role for [Ansible](https://github.com/ansible/ansible), that installs predefined set of packages on the system.

## Requirements

This role does not need any additional required packages.

## Quick start

1. First clone this repository and add into your project directory.
2. Include the role in your [Ansible](https://github.com/ansible/ansible) playbook.

## Example playbook

Example use of a role that installs a predefined set of packages on the system.

```yml
- hosts: all
  roles:
    - role: krudi.packages
      dependencies:
        - "git"
        - "nano"
        - "unzip"
        - "curl"
        - "wget"
```

## Issue

Have you found a bug in this project or have a suggestion for a new feature? Create a new ticket for the bug or feature, which can be found on the [GitHub](https://github.com/krudi/ansible-role-packages/issues) page.
