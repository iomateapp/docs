# Setup API Guide

## Requirements

A API foi desenvolvida para ser executada em Python com computação em nuvem sem servidor com os servidores da [AWS](https://aws.amazon.com/free/). 
Para efetuar o deploy ou executar o projeto localmente é necessário instalar o [Python3](https://www.python.org/downloads/) e [AWS CLI](https://aws.amazon.com/cli/). 
!!! warning

    Antes de prosseguir tenha certeza de que efetuou as seguintes instalações:

    - [GIT](https://git-scm.com/)
    
    - [Python3](https://www.python.org/downloads/)

    - [AWS CLI](https://aws.amazon.com/cli/)

Para mais informações de como configurar o AWS CLI confira o [Getting started with the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html).
    

## Configuration
### Cloning the repository
Clone o repositório da [API](https://github.com/iomateapp/api) em seu workspace.

```bash
git clone https://github.com/iomateapp/api.git
```

Ao finalizar abra o terminal e navegue até o diretório do projeto clonado.

### Instalando Dependencias
Comece isolando seu projeto em um [ambiente virtual](https://docs.python.org/3/library/venv.html).

```bash
python3 -m venv env
```

Ative o ambiente virtual criado para instalar a suas dependencias.

```bash
#Windows
./env/Scripts/Activate

# Linux / macOS
source ./env/bin/activate
```

Use o gerenciador de pacotes [pip3](https://pip.pypa.io/en/stable/) para instalar dependencias do projeto.

```bash
pip3 install -r requirements.txt
```

### Configurando o Serverless Framework
Utilizamos o [Serverless Framework](https://www.serverless.com/framework) para deploy e execução local do projeto.