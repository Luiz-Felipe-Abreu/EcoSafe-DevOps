
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

Abaixo estão os principais endpoints disponíveis na API:

#### Usuários
- `GET /usuarios` — Listar usuários
- `GET /usuarios/{id}` — Buscar usuário por ID
- `PUT /usuarios/{id}` — Atualizar usuário
- `DELETE /usuarios/{id}` — Remover usuário

#### Locais
- `GET /locais` — Listar locais
- `POST /locais` — Cadastrar novo local
- `GET /locais/{id}` — Buscar local por ID
- `PUT /locais/{id}` — Atualizar local
- `DELETE /locais/{id}` — Remover local

#### Sensores
- `GET /sensores` — Listar sensores
- `POST /sensores` — Cadastrar novo sensor
- `GET /sensores/{id}` — Buscar sensor por ID
- `PUT /sensores/{id}` — Atualizar sensor
- `DELETE /sensores/{id}` — Remover sensor

#### Leituras
- `GET /leituras` — Listar leituras
- `POST /leituras` — Registrar nova leitura
- `GET /leituras/{id}` — Buscar leitura por ID

#### Alertas
- `GET /alertas` — Listar alertas
- `GET /alertas/{id}` — Buscar alerta por ID

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

- 🎥 **Vídeo demonstrativo:** [Link aqui (quando disponível)]  

---/

