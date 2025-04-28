# Kindo Playbook

This is a setup playbook for Kindo project. It uses [PiOS Lite](https://www.raspberrypi.org/software/operating-systems/) as the base OS.

## Prerequisites

- PiOS Lite installed on a Raspberry Pi 4
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html)
- [uv](https://docs.astral.sh/uv/getting-started/installation/) - Python package manager

## Getting Started

### Development

1. Clone the repository to your local machine.

```bash
git clone https://github.com/KinTechnology/kindo-playbook
```

2. Sync the packages

```bash
uv sync
```

3. Run playbook

```bash
ansible-playbook --become main.yaml
ansible-playbook main.yaml --become -i inventory.ini
```

4. Run a specific tag

```bash
ansible-playbook main.yaml --tags docker --become -i inventory.ini
```

### Production

```bash
curl -fsL http://pkg.kintechnology.io/playbook | bash
```

## Contributing

To get started, please follow [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This project is licensed under a proprietary license. See [LICENSE](LICENSE) for more details.
