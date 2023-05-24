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

- Ansible: 2.10.8
- Fedora: 38
- XFCE: 4.18.0

## Commands

First we are located on the route:

```bash
$ cd ansible-fedora
```

Execution order:

1. **fedora-base.yml**:

```bash
$ ansible-playbook fedora-base.yml --ask-become-pass -i inventory/inventory.yml
```

2. **fedora-desktop.yml**:

```bash
$ ansible-playbook fedora-desktop.yml --ask-become-pass -i inventory/inventory.yml -e "ansible_python_interpreter=/usr/bin/python3"
```

3. **fedora-security.yml**:

```bash
$ ansible-playbook fedora-security.yml --ask-become-pass -i inventory/inventory.yml -e "ansible_python_interpreter=/usr/bin/python3"
```


## List

- [Fedora Packages](app-list.md)

## Fedora

- Fedora Offcial
- RPM Fusion

## Desktop Apps Extras

- [zoom](https://zoom.us/download#client_4meeting)
- [slack](https://slack.com/intl/en-bo/downloads/linux)
- [brave](https://brave.com/download/)
- [vscode](https://code.visualstudio.com/)
- [openvpn v3](https://community.openvpn.net/openvpn/wiki/OpenVPN3Linux)

## JS

- [nodejs](https://github.com/nodesource/distributions/blob/master/README.md)
- [yarn](https://classic.yarnpkg.com/lang/en/docs/install/#centos-stable)

## Containers

- [docker-ce](https://docs.docker.com/engine/install/fedora/)
- [helm](https://helm.sh/docs/intro/install/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)
- [docker-compose](https://github.com/docker/compose/releases)

## Cloud

- [aws](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-linux.html#cliv2-linux-install)
- [awless](https://github.com/wallix/awless/releases)
- [terraform](https://www.terraform.io/downloads.html)
- [packer](https://learn.hashicorp.com/tutorials/packer/get-started-install-cli)
- [assume-role](https://github.com/remind101/assume-role)
- [doctl](https://github.com/digitalocean/doctl)
- [terragrunt](https://github.com/gruntwork-io/terragrunt/releases)
- [gomplate](https://github.com/hairyhenderson/gomplate/releases)
- [hugo](https://github.com/gohugoio/hugo/releases)
- [opa](https://github.com/open-policy-agent/opa/releases)
- [popeye](https://github.com/derailed/popeye/releases)
- [sops](https://github.com/mozilla/sops/releases)
- [terraform-docs](https://github.com/terraform-docs/terraform-docs/releases)
- [terrascan](https://github.com/tenable/terrascan/releases)
- [tflint](https://github.com/terraform-linters/tflint/releases)
- [tfsec](https://github.com/aquasecurity/tfsec/releases)

## Data Bases

- [postgresql](https://www.postgresql.org/download/linux/redhat/)
- [mariadb](https://mariadb.org/download/?t=repo-config&d=Fedora+36+%28x86_64%29)
- [mysql](https://dev.mysql.com/downloads/repo/yum/)

## List of Repositories

