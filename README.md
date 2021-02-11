# macos-devbox

MacOS development box setup automated using Ansible playbook.

## Installation

1. Install [Homebrew](https://brew.sh/)

2. Clone this project

3. Install Ansible inside virtual environment

```sh
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

4. Install Ansible requirements

```sh
ansible-galaxy install -r requirements.yml
```

5. Run Ansible playbook

```sh
ansible-playbook local.yml
```
