# Kindo Playbook
This is a setup playbook for Kindo project. It uses [PiOS Lite](https://www.raspberrypi.org/software/operating-systems/) as the base OS.

## Prerequisites
- Raspberry Pi 4 with PiOS Lite installed
- Ansible installed on your Kindo
- Internet connection on your Raspberry Pi

## Getting Started

### Development
1. Clone the repository to your local machine.

```bash
git clone https://github.com/KinTechnology/kindo-playbook
```

2. Create/Use python virtual environment

```bash
python3 -m venv .venv && source .venv/bin/activate
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

4. Run playbook

```bash
ansible-playbook --become main.yaml
ansible-playbook main.yaml --become -i inventory.ini
```

5. Run a specific tag

```bash
ansible-playbook main.yaml --tags docker --become -i inventory.ini
```

### Production
1. Install Ansible on your Raspberry Pi

```bash
sudo apt install ansible -y
```

2. Run playbook

```bash
ansible-pull -U https://github.com/KinTechnology/kindo-playbook --become -i localhost, main.yaml
```

## Contributing
To get started, please follow [CONTRIBUTING.md](CONTRIBUTING.md).

## License
This project is licensed under a proprietary license. See [LICENSE](LICENSE) for more details.