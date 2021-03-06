# dotfiles

[![Actions Status](https://github.com/amz-x/dotfiles/workflows/DotfilesCI/badge.svg)](https://github.com/amz-x/dotfiles/actions)

Personal dotfiles on Fedora Linux with Ansible & Molecule.

![Screenshot](https://github.com/amz-x/dotfiles/raw/master/data/screenshot.png "Personal - Fedora 33 - Pantheon Desktop")

## Features

- Fedora 33
- ZSH
- Antibody
- NVM (Node Version Manager)
- Pantheon Desktop
- Visual Studio Code

## Additional Development Features

- Podman
- QEMU
- Vala

## Installation

### Setup Requirements

Requirements for installation setup on Fedora 30

- Fedora 33 Workstation
- Git
- Ansible

### Setup

Install Fedora 33 Workstation

Install ansible & git

```bash
sudo dnf install ansible git unzip -y
```

Download from Source

```bash
wget https://github.com/amz-x/dotfiles/archive/master.zip
```

Extract it

```bash
unzip master.zip -d dotfiles
```

### Installing

In root directory of project

```bash
ansible-playbook -K ./playbook.yml --connection=local --inventory 127.0.0.1, --limit 127.0.0.1
```

### Development Setup

Prerequisites

- python3
- python3-devel
- python3-pip
- python3-virtualenv

Setup

```bash
virtualenv .virtenv && source .virtenv/bin/activate && pip3 install -r requirements.txt
```

### Testing

```bash
cd ./setup
molecule test
```
