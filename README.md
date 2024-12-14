# 🚨 AppClimaMensageria

**AppClimaMensageria** é uma aplicação **Spring Boot** que permite a criação, envio e consulta de alertas climáticos. Com um fluxo interativo no terminal, você pode gerenciar alertas enquanto utiliza tecnologias modernas como **RabbitMQ** para mensageria e **PostgreSQL** como banco de dados relacional.

---

## 🛠️ Tecnologias Utilizadas

- **Java 17**  
- **Spring Boot 3.x**  
- **Hibernate** (JPA para persistência de dados)  
- **RabbitMQ** (mensageria)  
- **PostgreSQL** (banco de dados relacional)  
- **Maven** (gerenciador de dependências)  

---

## ✨ Funcionalidades

- **Envio de Mensagens de Alerta**  
  Insira dados como descrição, estado, nível de severidade, tipo de evento, latitude e longitude para criar alertas.

- **Visualização de Dados**  
  Consulte mensagens armazenadas diretamente no banco de dados através do terminal.

- **Mensageria com RabbitMQ**  
  O sistema utiliza filas do RabbitMQ para gerenciar a comunicação dos alertas.

- **Banco de Dados Relacional**  
  Os dados dos alertas são persistidos no PostgreSQL, gerenciado pelo Hibernate.


## 📋 Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas e configuradas no seu ambiente:

- **Java 17**  
- **PostgreSQL** (com uma base de dados configurada)  
- **RabbitMQ** (servidor de mensagens em execução)  
- **Maven**  

### Configurações do PostgreSQL

- Crie uma base de dados chamada `clima_mensageria`.  
- Atualize o arquivo `application.properties` com suas credenciais:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/clima_mensageria
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
