📚 Sistema de Gerenciamento de Cursos

Este é um projeto simples desenvolvido com Spring Boot + Spring Data JPA + MySQL, utilizando Java 21.
O objetivo é gerenciar cursos com os seguintes campos:

id (Long)

nome (String)

categoria (Enum)

descricao (String)



---

🚀 Tecnologias Utilizadas

Tecnologia	Versão

Java	21
Spring Boot	3.5.8
Maven	Sim
MySQL	8+



---

📂 Estrutura do Projeto

src/
 └── main/
     ├── java/com/example/cursos/
     │     ├── CursosApplication.java  // MAIN para rodar
     │     ├── controller/             // REST API
     │     ├── dto/                    // DTOs
     │     ├── model/                  // Entidades (JPA)
     │     ├── repository/             // Repository (JPA)
     │     └── service/                // Regras de negócio
     └── resources/
           ├── application.yml         // Configurações do Spring + MySQL
           └── data.sql (opcional)


---

⚙️ Configuração do application.yml

server:
  port: 8080

spring:
  datasource:
    url: jdbc:mysql://localhost:3306/fullstack?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=UTC
    username: root
    password: MySQL
    driver-class-name: com.mysql.cj.jdbc.Driver

  jpa:
    hibernate:
      ddl-auto: update
    properties:
      hibernate:
        show_sql: true
        format_sql: true


---

▶️ Como Rodar o Projeto

✔️ Pelo IntelliJ / Eclipse / VSCode

Basta abrir o projeto e rodar a classe:

CursosApplication.java

✔️ Pelo terminal com Maven

mvn spring-boot:run


---

🔗 Endpoints da API

Método	Endpoint	Descrição

GET	/cursos	Lista todos os cursos
POST	/cursos	Cadastra um novo curso
GET	/cursos/{id}	Busca por ID
DELETE	/cursos/{id}	Remove curso



---

📌 Exemplo de JSON para POST

{
  "nome": "Java Spring Boot",
  "categoria": "PROGRAMACAO",
  "descricao": "Curso de backend"
}


---

📌 Possíveis Melhorias

Swagger (Documentação da API)

Banco em Docker

DTO com validação @Valid

Relacionamento com Aluno (OneToMany)



---
