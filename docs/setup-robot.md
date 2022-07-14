# Setup API Guide

## Requisitos

O Robot foi desenvolvido para ser executada em Python em estações de trabalhos convencionais. 
Para executar o projeto é necessário instalar os requisitos listados abaixo. 
!!! warning

    Antes de prosseguir tenha certeza de que efetuou as seguintes instalações:

    - [GIT](https://git-scm.com/)
    
    - [Python3](https://www.python.org/downloads/)


## Configuração
### Clonando o repositório
Clone o repositório da [API](https://github.com/iomateapp/api) em seu workspace.

```bash
git clone https://github.com/iomateapp/robot
```

Ao finalizar abra o terminal e navegue até o diretório do projeto clonado.
```bash
cd robot
```

### Instalando as dependências
Comece isolando seu projeto em um [ambiente virtual](https://docs.python.org/3/library/venv.html).

```bash
python3 -m venv env
```

Ative o [ambiente virtual](https://docs.python.org/3/library/venv.html) criado para instalar a suas dependências.

=== "Windows"

    ``` bash
    ./env/Scripts/Activate
    ```

=== "Linux / MacOS"
    ``` bash 
    source ./env/bin/activate
    ```

Use o gerenciador de pacotes [pip3](https://pip.pypa.io/en/stable/) para instalar as dependências do projeto.

```bash
pip3 install -r requirements.txt
```

## Execução
Para iniciar o projeto é necessário executar o arquivo `robot.py`.
```bash
python3 robot.py
```