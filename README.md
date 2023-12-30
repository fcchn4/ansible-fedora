# ANSIBLE INSTALL

This repository contains a list of packages for the Fedora distribution. Contains a list of packages with repositories, desktop packages, and devops tools.

## Pre-Requisites

First we must manually execute the following commands on the computer where the installation will take place:

```bash
$ sudo systemctl enable --now sshd.service
```

Then we must copy a public SSH key on the computer where the installations will be executed:

```bash
$ ssh-copy-id -o PubkeyAuthentication=no -i ~/.ssh/demo-ssh.pub user_name@ip_address_or_localhost
```

This ansible poroject is for automatic install on post-installation for Fedora Operating System.

## Config Files and replace values

The project have three playbooks:

- fedora-base.yml
- fedora-desktop.yml
- fedora-security.yml

## Versions

- Ansible: 2.16.2
- Fedora: 39
- XFCE: 4.18.0

## Commands

First we are located on the route:

```bash
$ cd ansible-fedora
```

Execution order:

1. **fedora-base.yml**:

```bash
$ ansible-playbook fedora-base.yml -i inventory/inventory.yml
```

2. **fedora-desktop.yml**:

```bash
$ ansible-playbook fedora-desktop.yml -i inventory/inventory.yml
```

3. **fedora-security.yml**:

```bash
$ ansible-playbook fedora-security.yml -i inventory/inventory.yml
```

Exmaples flags for ansible command:

```bash
--ask-become-pass # If you need sudo privileges, is necessary for fedora-base.yml
-e "ansible_python_interpreter=/usr/bin/python3" # Specific Python version
```

## Fedora

- Fedora Offcial
- RPM Fusion
- [Fedora Packages](/details-md/app-list-official.md)

## Extra Packages

- [List Extra Packages](/details-md/app-list-extras.md)
