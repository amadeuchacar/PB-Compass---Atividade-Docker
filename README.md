# (PB Compass) - Atividade Docker - DevSecOps
### Atividade realizada por Amadeu Chacar e Rodrigo Pacheco

## Objetivo
*Subir uma aplicação Wordpress + DB Mysql utilizando docker, com requisito da aplicação Wordpress estar rodando na porta 80 ou 8080*

# 🔨 Instalação do Docker Desktop 
*Para a realização da atividade proposta é necessário que o Docker Desktop esteja funcionando perfeitamente na máquina*

## Requisitos
- WSL 2 (Linux que roda dentro do windowws)
- Caso necessário, habilitar a virtualização na BIOS
- Windows 11 de 64 bits: Home ou Pro versão 21H2 ou superior, ou Enterprise ou Education versão 21H2 ou superior
- Windows 10 de 64 bits: Home ou Pro 21H1 (build 19043) ou superior, ou Enterprise ou Education 20H2 (build 19042) ou superior
- Processador de 64 bits com tradução de endereço de segundo nível (SLAT)
- 4GB de RAM do sistema

Download Docker Desktop: https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe

## 1. Configuração 
### 1.1 Após feita a instalação, execute o Docker Desktop
### 1.2 Vá em configurações 
### 1.3 General 
### 1.4 Certifique-se que as abas "Use WSL 2 based engine" e "Use Docker Compose V2" estejam marcadas 

## 2. Instalação do WSL 2
### 2.1 Abra o PowerShell e habilite os recursos necessários para executar o WSL e instalar distribuição Ubuntu do Linux 
```ruby
wsl --install
```

### 2.2 Verificar a versão do  WSL instalada
```ruby
wsl -l -v
```
### 2.3 Caso seja a versão 1 instalada, altere para versão 2
```ruby
wsl --set-default-version 2
```
### 2.4 Executar WSL (executa o linux dentro do PowewerShell)
```ruby
wsl.exe
```
# 🖥 Executando a aplicação 

## 1. Criação do projeto
### 1.1 Necessário criar um diretório para o projeto
### 1.2 Criar um arquivo docker-compose.yml (ou .yaml) dentro do diretório 

## 2. Definindo o arquivo docker-compose.yml
### 2.1 Utilizando algum editor de texto, definir o arquivo docker-compose.yml e suas especificações
### 2.2 docker-compose.yml vai definir o wordpress e o mysql
### 2.3 O arquivo docker-compose.yml está presente no repositório 

## 3. Executar o projeto 
### 3.1 Entrar no diretório em que o docker-compose.yml está localizado, e executar:
```ruby
docker compose up -d
```
### *Este comando cria e executa em segundo plano os containers de Wordpress e Mysql especificados*

## 4. Acessar o Wordpress
### 4.1 Após a execução, o Wordpress estará rodando na porta especificada no arquivo docker-compose, no caso do exemplo, na porta 80
### 4.2 Acessar no navegador o link: http://localhost:80
### 4.3 Configurar o Wordpress: idioma, nome de usuário e senha
### 4.4 Instalar o Wordpress
### 4.5 Acessá-lo
### 4.6 É possível acessar a página de login nesse endereço: http://localhost:80/wp-admin/

## 5. Alterando nome do endereço do site 
### 5.1 Acesse o diretório: C:\Windows\System32\drivers\etc\hosts
### 5.2 Execute o hosts como administrador para poder realizar as alterações
### 5.3 Adicione um endereço de acordo com o IP do Docker Desktop
### 5.4 Exemplo: 192.168.0.194 exemplo.com
### 5.5 Salve e acesse http://exemplo.com:80/wp-admin/

## 6. Acessando o Banco de Dados 
### 6.1 É possível acessar o MySQL com o phpMyAdmin contido no docker-compose deste repositório 
### 6.2 Acesse: http://exemplo.com:8080 

----------------------------------------------------------------------------------------------------------------------------------------------------------

## Algumas observações 
- O comando *docker compose down* remove os containers e a rede padrão mas preserva a base de dados do wordpress
- O comando *docker compose down –-volumes* remove também a base de dados




