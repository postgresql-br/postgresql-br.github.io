### 0) Instalando dependências

sudo apt install git make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils

### 1) Instalando pyenv

git clone https://github.com/pyenv/pyenv.git ~/.pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
source ~/.bashrc

### 2) Instalando Python 3.5.2

pyenv install 3.5.2

### 4) Instalando Pelican

pip install pelican
pip install markdown

### 5) Construção

make html

O conteúdo estático estará na pasta `output`.

### 6) Desenvolvimento

make devserver

Construirá o conteúdo estático e iniciará um servidor web local na porta 8000. Para parar o servidor:

make stopserver
