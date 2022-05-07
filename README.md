# Ansible Install Linux

This repository contains a list of packages for Fedora, Debian, and Ubuntu distributions. It only contains a long list of packages for some GNU/Linux distributions.

## List

- [Fedora Packages](fedora-software.md)

## Fedora 34

## Packages Extra no Included

- [zoom](https://zoom.us/download#client_4meeting)
- [slack](https://slack.com/intl/en-bo/downloads/linux)
- [brave](https://brave.com/download/)
- [aws](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-linux.html#cliv2-linux-install)
- [awless](https://github.com/wallix/awless/releases)
- [helm](https://helm.sh/docs/intro/install/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)
- [terraform](https://www.terraform.io/downloads.html)
- [packer](https://learn.hashicorp.com/tutorials/packer/get-started-install-cli)
- [assume-role](https://github.com/remind101/assume-role)
- [doctl](https://github.com/digitalocean/doctl)

## List of Repositories

### Fedora

- Fedora Offcial
- RPM Fusion
- VSCode
- Docker CE
- Yarn
- Postgresql
- Terraform
- Kubectl

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

- Ansible: 2.9
- Fedora: 34
- XFCE: 4.16.0

## Commands

First we are located on the route:

```bash
$ cd ansible-fedora
```

Execution order:

1. **fedora-base.yml**:

```bash
$ ansible-playbook fedora-base.yml \
--ask-become-pass \
-i inventory/inventory.yml
```

2. **fedora-desktop.yml**:

```bash
$ ansible-playbook fedora-desktop.yml \
--ask-become-pass \
-i inventory/inventory.yml \
-e "ansible_python_interpreter=/usr/bin/python3"
```

3. **fedora-security.yml**:

```bash
$ ansible-playbook fedora-security.yml \
--ask-become-pass \
-i inventory/inventory.yml \
-e "ansible_python_interpreter=/usr/bin/python3"
```
