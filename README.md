# (CompassPB) - Atividade Docker - DevSecOps
### Atividade realizada por Amadeu Chacar e Rodrigo Pacheco

## Objetivo
Subir uma aplicação Wordpress + DB Mysql utilizando docker, com requisito da aplicação Wordpress estar rodando na porta 80 ou 8080

# Instalação do Docker Desktop
Para a realização da atividade proposta é necessário que o Docker Desktop esteja funcionando perfeitamente na máquina

## Requisitos
- WSL 2 (Linux que roda dentro do windowws)
- Caso necessário, habilitar a virtualização na BIOS
- Windows 11 de 64 bits: Home ou Pro versão 21H2 ou superior, ou Enterprise ou Education versão 21H2 ou superior
- Windows 10 de 64 bits: Home ou Pro 21H1 (build 19043) ou superior, ou Enterprise ou Education 20H2 (build 19042) ou superior
- Processador de 64 bits com tradução de endereço de segundo nível (SLAT)
- 4GB de RAM do sistema

Download Docker Desktop: https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe

## Configuração 
### 1- Após feita a instalação, execute o Docker Desktop
### 2- Vá em configurações 
### 3- General 
### 4- Certifique-se que as abas "Use WSL 2 based engine" e "Use Docker Compose V2" estejam marcadas 

## Instalação do WSL 2
### 1- Abra o PowerShell
wsl --install (habilita os recursos necessários para executar o WSL e instalar a distribuição Ubuntu do Linux)

### 2- Verificar a versão do  WSL instalada
wsl -l -v
### 3- Caso seja a versão 1 instalada, altere para versão 2
wsl --set-default-version 2
### 4- Executar WSL 
wsl.exe (executa o linux dentro do PowewerShell)

# Executando a aplicação

## Criação do projeto
### 1- Necessário criar um diretório para o projeto
### 2- Criar um arquivo docker-compose.yml (ou .yaml) dentro do diretório 
----------------------------------------------------------------------------------------------------------------------------------------------------------
## Definindo o arquivo docker-compose.yml
### 1- Utilizando algum editor de texto, definir o arquivo docker-compose.yml e suas especificações
### 2- docker-compose.yml vai definir o wordpress e o mysql
### 3- O arquivo docker-compose.yml está presente no repositório 
----------------------------------------------------------------------------------------------------------------------------------------------------------
## Executar o projeto 
### 1- Após a definição do arquivo docker-compose, dentro do diretório em que ele está localizado, executá-lo através do comando docker compose up -d
### 2- Este comando irá criar e executar em segundo plano os containers de Wordpress e Mysql especificados
----------------------------------------------------------------------------------------------------------------------------------------------------------
## Acessar o Wordpress
### 1- Após a execução, o Wordpress estará rodando na porta especificada no arquivo docker-compose, no caso do exemplo, na porta 80
### 2- Acessar no navegador o link: http://localhost:80
### 3- Configurar o Wordpress: idioma, nome de usuário e senha
### 4- Instalar o Wordpress
### 5- Acessá-lo
----------------------------------------------------------------------------------------------------------------------------------------------------------

## Algumas observações 
- O comando docker compose down remove os containers e a rede padrão mas preserva a base de dados do wordpress
- O comando docker compose down –volumes remove também a base de dados
