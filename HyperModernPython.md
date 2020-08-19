# Hypermodern Python according to [Claudio Jolowicz's](https://cjolowicz.github.io/posts/hypermodern-python-01-setup/) post :

```BASH
sudo apt update && sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```
Install the  developer environment :
```BASH
curl https://pyenv.run | bash

```

copy this in the ~/.bashrc :

```
export PATH="~/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

```BASH
sudo apt update && sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```

Install the developpement environnement :
```BASH
pyenv install 3.8.2
pyenv install 3.7.7
pyenv local 3.8.2 3.7.7
```

Install Poetry
```BASH
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python
source ~/.poetry/env
poetry init --no-interaction
```

```BASH
cat requirements.txt | cut -d "=" -f1 | while read -r data; do  poetry add $data; done
```