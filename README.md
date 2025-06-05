
'# 🌱 EcoSafe - Solução Tecnológica para Eventos Climáticos Extremos

## 💡 Sobre o Projeto

**EcoSafe** é uma aplicação desenvolvida como parte do desafio da **Global Solution FIAP 2025**, com o objetivo de criar uma solução tecnológica inovadora para enfrentar **eventos climáticos extremos**.

A proposta foca no **monitoramento de locais sensíveis** por meio de sensores e geração de **alertas automáticos** baseados nas leituras. Com isso, buscamos **ajudar comunidades vulneráveis**, fornecendo **informações em tempo real** para promover ações preventivas e respostas rápidas a desastres naturais.

A aplicação oferece uma **API RESTful** robusta que gerencia:

- Usuários  
- Locais  
- Sensores  
- Leituras  
- Alertas em tempo real  

Integra-se a um banco de dados **PostgreSQL** conteinerizado, garantindo portabilidade e escalabilidade.

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

Com os containers rodando, acesse a documentação interativa via Swagger:

👉 [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

---

### 🛑 Parar e remover os containers

Execute:

```bash
docker-compose down -v
```

> 🔸 Isso irá parar e remover os containers e os volumes, limpando todo o ambiente.

---

## ✅ Funcionalidades Implementadas

- 🔐 Registro e login de usuários com **autenticação JWT**
- 📍 **Cadastro de locais e sensores**
- 📈 **Registro de leituras dos sensores**
- 🚨 **Geração de alertas automáticos** com associação aos usuários
- 🔄 **CRUD completo** para entidades principais:
  - Usuário
  - Local
  - Sensor
  - Alerta
- 🧪 Documentação interativa da API via **Swagger**

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
| [Seu Nome]         | [Seu RM]  |
| [Integrante 2]     | [RM]      |
| [Integrante 3]     | [RM]      |
| [Integrante 4]     | [RM]      |

---

## 📹 Extras

- 🎥 **Vídeo demonstrativo:** [Link aqui (quando disponível)]  
- 🔗 **Repositório:** [https://github.com/seu-usuario/ecosafe](https://github.com/seu-usuario/ecosafe)  

---

## 🤝 Licença

Este projeto é de uso acadêmico para a FIAP e não possui fins comerciais.'
