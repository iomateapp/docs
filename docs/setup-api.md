# Setup API Guide

## Requisitos

A API foi desenvolvida para ser executada em Python com [computação em nuvem sem servidor](https://aws.amazon.com/serverless/) com os serviços da [AWS](https://aws.amazon.com/free/). 
Para efetuar o deploy ou executar o projeto localmente é necessário instalar os requisitos listados abaixo. 
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

### Configurando o MongoDB
O projeto IOmate utiliza o [MongoDB](https://www.mongodb.com/) para armazenamento e transição de dados. Para executar a aplicação é necessário de uma instância do banco de dados à disposição. É possível utilizar o [MongoDB SAAS](https://www.mongodb.com/try) ou instalar e configurar o [MongoDB localmente](https://www.mongodb.com/try/download).


### Configurando o Serverless Framework
Para publicar ou executar localmente o projeto utilizamos o [Serverless Framework](https://www.serverless.com/framework).

Instale os plugins do [Serverless Framework](https://www.serverless.com/framework) utilizados no projeto para publicar e executar a API.
```bash
npm install
```

Após instalar os plugins é necessário configurar as variáveis de ambiente. Para isso você deve criar um arquivo `.env` na raiz do seu projeto. O arquivo `.env` deve seguir o exemplo abaixo substituindo os valores da sua aplicação.
```bash
MONGO_URI=mongodb+srv://user:password@example.example.net
```

!!! warning

    O arquivo `.env` contém todos os dados sensíveis da aplicação, por esse motivo jamais compartilhe esse documento.


## Execução e Publicação
### Executar Offline
Para executar o projeto na rede local execute o [Serverless Framework](https://www.serverless.com/framework) no modo offline.
```bash
serverless offline
```

### Publicar
Para publicar o projeto com a sua conta AWS utilize o [Serverless Framework](https://www.serverless.com/framework).

Instalação com `stage` e `region` informados no `serverless.yml`:
```bash
serverless deploy
```

Instalação com `stage` e `region` personalizados:
```bash
serverless deploy --stage {custom_stage} --region {custom_region}
```