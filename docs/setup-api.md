# Setup API Guide

## Requisitos

A API foi desenvolvida para ser executada em Python com [computação em nuvem sem servidor](https://aws.amazon.com/serverless/) com os serviços da [AWS](https://aws.amazon.com/free/). 
Para efetuar o deploy ou executar o projeto localmente é necessário instalar o [Python3](https://www.python.org/downloads/) e [AWS CLI](https://aws.amazon.com/cli/). 
!!! warning

    Antes de prosseguir tenha certeza de que efetuou as seguintes instalações:

    - [GIT](https://git-scm.com/)
    
    - [Python3](https://www.python.org/downloads/)

    - [AWS CLI](https://aws.amazon.com/cli/)

    - [Serverless Framework](https://www.serverless.com/framework)

Para mais informações de como configurar o AWS CLI confira o [Getting started with the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html).
    

## Configuração
### Clonando o repositório
Clone o repositório da [API](https://github.com/iomateapp/api) em seu workspace.

```bash
git clone https://github.com/iomateapp/api.git
```

Ao finalizar abra o terminal e navegue até o diretório do projeto clonado.

### Instalando as dependências
Comece isolando seu projeto em um [ambiente virtual](https://docs.python.org/3/library/venv.html).

```bash
python3 -m venv env
```

Ative o ambiente virtual criado para instalar a suas dependências.

```bash
#Windows
./env/Scripts/Activate

# Linux / macOS
source ./env/bin/activate
```

Use o gerenciador de pacotes [pip3](https://pip.pypa.io/en/stable/) para instalar as dependências do projeto.

```bash
pip3 install -r requirements.txt
```

### Configurando o Serverless Framework
Utilizamos o [Serverless Framework](https://www.serverless.com/framework) para publicar e executar localmente o projeto.

Instale os plugins utilizados no projeto para conseguir publicar e executar a API.
```bash
serverless plugin install -n serverless-python-requirements
serverless plugin install -n serverless-offline
```


## Execução e Publicação
### Executar Offline
Para executar o projeto na rede local execute o [Serverless Framework](https://www.serverless.com/framework) no modo offline.
```bash
serverless offline
```

### Publicar
Para publicar o projeto com a sua conta AWS utilize o [Serverless Framework](https://www.serverless.com/framework).

```bash
serverless deploy
```