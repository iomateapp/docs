# Setup API Guide

## Requisitos

The API was built with and designed to run [serverless with AWS services](https://aws.amazon.com/serverless/). 

!!! warning

    To proceed with the next steps, you need to follow these prerequisites

    - [GIT](https://git-scm.com/)
    
    - [Python3](https://www.python.org/downloads/)

    - [AWS CLI](https://aws.amazon.com/cli/)

    - [Serverless Framework](https://www.serverless.com/framework)

For more information on how to configure the AWS CLI we recommend that you take a look at the [Official Documentation](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html).

## Configuration

### Clonning the repository
Clone the repository into your workspace.

```bash
git clone https://github.com/{your_user}/api.git
```

After finishing, navigate to the project directory.
```bash
cd api
```

### Installing dependencies
Start by isolating your project in a [virtual environment](https://docs.python.org/3/library/venv.html).

```bash
python3 -m venv env
```

Activate the [virtual environment](https://docs.python.org/3/library/venv.html) created to install your dependencies.

=== "Windows"

    ``` bash
    ./env/Scripts/Activate
    ```

=== "Linux / MacOS"
    ``` bash 
    source ./env/bin/activate
    ```

Use the package manager [pip3](https://pip.pypa.io/en/stable/) to install the project dependencies.

```bash
pip3 install -r requirements.txt
```

### Configurando o MongoDB
The IOmate uses [MongoDB](https://www.mongodb.com/) for data storage and transition. 
Para executar a aplicação é necessário de uma instância do banco de dados à disposição. É possível utilizar o [MongoDB SAAS](https://www.mongodb.com/try) ou instalar e configurar o [MongoDB localmente](https://www.mongodb.com/try/download).


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