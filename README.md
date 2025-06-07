
'# 🌱 EcoSafe - Solução Tecnológica para Eventos Climáticos Extremos

## 💡 Sobre o Projeto

**EcoSafe** é uma aplicação desenvolvida como parte do desafio da **Global Solution FIAP 2025**, com o objetivo de criar uma solução tecnológica inovadora para enfrentar **eventos climáticos extremos**.

A proposta foca no **monitoramento de locais sensíveis** por meio de sensores e geração de **alertas automáticos** baseados nas leituras. Com isso, buscamos **ajudar comunidades vulneráveis**, fornecendo **informações em tempo real** para promover ações preventivas e respostas rápidas a desastres naturais.

---

## 🛠️ Tecnologias Utilizadas

- ✅ **Java 17**  
- ✅ **Spring Boot**  
- ✅ **Spring Data JPA**  
- ✅ **Swagger (OpenAPI)**  
- ✅ **PostgreSQL**  
- ✅ **Docker & Docker Compose**  
- ✅ **Maven**  
- ✅ **JWT (Autenticação)**  
- ✅ **Lombok**  

---

## 🚀 Como Executar o Projeto

### 🔧 Pré-requisitos
- Java 17+
- Maven
- Docker e Docker Compose

---

### 🔨 Build da aplicação

Execute no terminal:

```bash
mvn clean package -DskipTests
```

> 🔸 Esse comando gera o arquivo `.jar` da aplicação, ignorando os testes.

---

### 🐳 Subir a aplicação com Docker

Execute:

```bash
docker-compose up --build -d
```

Esse comando irá:

- Construir a imagem da aplicação (Dockerfile)  
- Subir o banco de dados PostgreSQL com volume persistente  
- Executar ambos os containers em segundo plano (`-d`)

---

### 📑 Acessar a API

Abaixo estão os principais endpoints disponíveis na API (exemplo de URL: `http://localhost:8080`):

#### Usuários
- `GET http://localhost:8080/api/usuarios` — Listar usuários (paginado)
- `GET http://localhost:8080/api/usuarios/{id}` — Buscar usuário por ID
- `POST http://localhost:8080/api/usuarios` — Cadastrar novo usuário
- `PUT http://localhost:8080/api/usuarios/{id}` — Atualizar usuário
- `DELETE http://localhost:8080/api/usuarios/{id}` — Remover usuário
- `GET http://localhost:8080/api/usuarios/buscar?nome={nome}` — Buscar usuários por nome (paginado)

#### Locais
- `GET http://localhost:8080/api/locais` — Listar locais (paginado)
- `GET http://localhost:8080/api/locais/{id}` — Buscar local por ID
- `POST http://localhost:8080/api/locais` — Cadastrar novo local
- `PUT http://localhost:8080/api/locais/{id}` — Atualizar local
- `DELETE http://localhost:8080/api/locais/{id}` — Remover local
- `GET http://localhost:8080/api/locais/buscar/cidade?cidade={cidade}` — Buscar locais por cidade (paginado)

#### Sensores
- `GET http://localhost:8080/api/sensores` — Listar sensores (paginado)
- `GET http://localhost:8080/api/sensores/{id}` — Buscar sensor por ID
- `POST http://localhost:8080/api/sensores` — Cadastrar novo sensor
- `PUT http://localhost:8080/api/sensores/{id}` — Atualizar sensor
- `DELETE http://localhost:8080/api/sensores/{id}` — Remover sensor
- `GET http://localhost:8080/api/sensores/buscar/tipo?tipo={tipo}` — Buscar sensores por tipo (paginado)
- `GET http://localhost:8080/api/sensores/buscar/status?status={status}` — Buscar sensores por status (paginado)

#### Leituras
- `GET http://localhost:8080/api/leituras` — Listar leituras (paginado)
- `GET http://localhost:8080/api/leituras/{id}` — Buscar leitura por ID
- `POST http://localhost:8080/api/leituras` — Registrar nova leitura
- `GET http://localhost:8080/api/leituras/buscar?sensorId={id}` — Buscar leituras por sensor (paginado)

#### Alertas
- `GET http://localhost:8080/api/alertas` — Listar alertas (paginado)
- `GET http://localhost:8080/api/alertas/{id}` — Buscar alerta por ID

---

### 🗄️ Acessar o Banco de Dados PostgreSQL

Siga os passos abaixo para acessar o banco de dados, consultar tabelas e sair:

1. **Acesse o container do banco de dados via terminal:**

   ```bash
   docker exec -it eco-postgres psql -U postgres -d eco_safe
   ```

2. **Liste os dados de uma tabela (substitua `nome_da_tabela` pelo nome desejado):**

   ```sql
   SELECT * FROM nome_da_tabela;
   ```

3. **Para sair do PostgreSQL, digite:**

   ```
   \q
   ```

---

### 🛑 Parar e remover os containers

Execute:

```bash
docker-compose down -v
```

> 🔸 Isso irá parar e remover os containers e os volumes, limpando todo o ambiente.

---

## ✅ Funcionalidades Implementadas

- 📍 **Cadastro de locais e sensores**
- 📈 **Registro de leituras dos sensores**
- 🚨 **Geração de alertas automáticos** com associação aos usuários
- 🔄 **CRUD completo** para entidades principais:
  - Usuário
  - Local
  - Sensor
  - Alerta

---

## 📂 Estrutura do Projeto

```
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.ecosafe
│   │   │       ├── config
│   │   │       ├── controller
│   │   │       ├── dto
│   │   │       ├── model
│   │   │       ├── repository
│   │   │       └── service
│   │   └── resources
│   │       ├── application.yml
│   │       └── ...
├── Dockerfile
├── docker-compose.yml
├── README.md
└── pom.xml
```
---

## 👥 Equipe

| Nome               | RM        |
| ------------------ | --------- |
| Luiz Felipe         | 555197  |
| Pedro Gomes     | 553907      |
| Matheus Munuera     | 557812      |


---

## 📹 Extras

- 🎥 **Vídeo demonstrativo:** https://www.youtube.com/watch?v=vkDcPXFDwvU&ab_channel=LuizFelipe

---/

