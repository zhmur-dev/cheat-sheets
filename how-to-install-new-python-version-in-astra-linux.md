# How to install new Python version in Astra Linux
---
## Step 1: bash
```bash
sudo apt install curl -y
curl https://pyenv.run | bash
```
## Step 2: nano ~/.bashrc
```bash
#pyenv
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```
## Step 3: bash
```bash
sudo apt update; sudo apt install build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev curl \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```
## Step 4: bash
```bash
pyenv install 3.12.0  #type in the required version instead of 3.12.0
pyenv global 3.12.0  #type in the required version instead of 3.12.0
```
---
## Enjoy !

