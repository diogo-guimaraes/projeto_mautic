
# Mautic

## Ambientação e instalação

### Ambientação
----------------

#### Passo 1 - clonando o repositório do Mautic
-----------------------------------------------

Utilizando o git bash, clone o repositório mautic no seu ambiente de desenvolvimento, executando o seguinte comando:

```sh
$ git clone -b staging https://github.com/mautic/mautic.git mautic
```

#### Passo 2 - instalando o composer
-------------------------------------

Inicie o git bash dentro da pasta clonada do mautic e execute o seguinte comando:

```sh
$ composer install
```

#### Passo 3 - configurando o PHP
----------------------------------

* Abra o arquivo php.ini localizado na pasta do seu PHP
* Busque pelo paramentro: max_execution_time
* Mude o valor para 300

### Instalação

#### Passo 1 - iniciando a instalação do Mautic
--------------------------------------------------
Utilizando o browser, com o apache ativado, acesse a pasta do projeto Mautic  através do seguinte caminho:

```sh
https://localhost/mautic/
```

 A instalação será iniciada

* EM MAUTIC INSTALLATION - CHECK

Apenas clique em => Next Step

#### Passo 2 - configurando o banco de dados
--------------------------------------------

```shell
 Database driver: Matenha a opção Mysql PDO.
 Database host: "localhost"
 Database port: "3306"
 Database name: "munic"
 Database Table Prefix: "munic_"
 Database Username: "root"
 Database Password: "" (Campo vazio - para quem não usa senha no localhost)  
 back up existing?: "No"
```

Apenas clique em => Next Step
  
#### Passo 3 - criando usuário para acesso ao Munic
---------------------------------------------------

```shell
Admin username: "admin"
Admin password: "mautic"
Database port: "3306"
First name: "Nome"
Last name: "Sobrenome"
E-mail: "seuemail@exemplo.com"
```

Apenas clique em => Next Step

#### Passo 4 - configurando e-mail
----------------------------------

```shell
How Shold the email be sent as?: "Nome Completo"
E-mail: "seuemail@exemplo.com"
E-mail handling: "send immediately"
Mailer transport: "PHP Mail"
```
Apenas clique em => Next Step

## Configuração interna

### Alterarando avatar

Subir uma foto no https://br.gravatar.com/ com o mesmo emaiil que usou no cadastro do mautic  

### Alterando o idioma

Após alterar o idioma, aplicar e salvar, se o idioma não atualizar:

* faça logout
* No terminal, na pasta do projeto execute

```shell
php app/console cache:clear"
```