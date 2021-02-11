# macos-devbox

MacOS development box setup automated using Ansible playbook.

## Installation

1. Install [Homebrew](https://brew.sh/)

2. Clone this project:

```sh
mkdir -p $HOME/Projects/github/bwilczynski && cd $_
git clone https://github.com/bwilczynski/macos-devbox.git && cd macos-devbox
```

3. Install Ansible inside virtual environment

```sh
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

On Apple M1, or if the installation fails because cryptography wheel cannot be found you might want to build it from sources:

https://cryptography.io/en/latest/installation.html

```sh
brew install openssl@1.1 rust
env LDFLAGS="-L$(brew --prefix openssl@1.1)/lib" CFLAGS="-I$(brew --prefix openssl@1.1)/include" pip install -r requirements.txt
```

4. Install Ansible requirements

```sh
ansible-galaxy install -r requirements.yml
```

5. Run Ansible playbook

```sh
ansible-playbook local.yml
```
