# ProjetoWebAula27 - CRUD de Usuários

Este projeto implementa um CRUD de Usuários utilizando Node.js, PostgreSQL e Docker.  
Ele é composto por três partes principais:

- backend/ → API em Node.js responsável pelas operações do CRUD.  
- frontend/ → Interface web em HTML + JavaScript para interação com a API.  
- db/ → Configuração do banco de dados PostgreSQL e script de inicialização.  

A orquestração é feita com Docker Compose, permitindo subir todo o ambiente com apenas um comando.

------------------------------------------------------------

## Estrutura do Projeto

ProjetoWebAula27/
├── backend/        # API em Node.js
│   ├── server.js
│   ├── package.json
│   ├── Dockerfile
│   └── ...
│
├── frontend/       # Interface web
│   ├── index.html
│   ├── app.js
│   └── Dockerfile
│
├── db/             # Banco de dados
│   └── init.sql
│
├── docker-compose.yml
└── .env            # Variáveis de ambiente

------------------------------------------------------------

## Pré-requisitos

- Docker instalado  
- Docker Compose instalado  

------------------------------------------------------------

## Como Executar o Projeto

1. Clone o repositório:

   git clone https://github.com/mackleyrf/ProjetoWebAula27.git
   cd ProjetoWebAula27

2. Suba todos os serviços (backend, frontend e banco) com:

   docker-compose up --build

3. Acesse no navegador o frontend:

   http://localhost:8080

   (ou a porta definida no docker-compose.yml)

------------------------------------------------------------

## Serviços

- Frontend (porta 8080) → Interface do CRUD para interação com a API  
- Backend (porta 3000) → API em Node.js responsável pelas rotas CRUD  
- Postgres (porta 5432) → Banco de dados relacional, inicializado via init.sql  

------------------------------------------------------------

## Funcionalidades

- Criar, ler, atualizar e deletar usuários  
- Listagem dinâmica no frontend  
- Integração completa entre Node.js + PostgreSQL  
- Orquestração com Docker Compose  

------------------------------------------------------------

## Tecnologias Utilizadas

- Node.js + Express (API)  
- PostgreSQL (Banco de dados)  
- HTML, CSS e JS (Frontend)  
- Docker & Docker Compose (Infraestrutura)  

------------------------------------------------------------

## Comandos Úteis do Docker

- Subir os containers:  
  docker-compose up --build

- Parar os containers:  
  docker-compose down

- Ver logs de um serviço:  
  docker-compose logs -f backend

- Acessar o banco de dados dentro do container:  
  docker exec -it <nome_container_postgres> psql -U postgres -d postgres

------------------------------------------------------------

Projeto desenvolvido para fins acadêmicos. Disciplina: PROGRAMAÇÃO AVANÇADA PARA WEB
