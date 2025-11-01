# Documento de Arquitetura

## Histórico de Versão

| Data       | Versão | Descrição                                | Autor(es)      |
| ---------- | ------ | ---------------------------------------- | -------------- |
| 1/11/2025 | 1.0    | Criação do documento de arquitetura      | Pedro Vargas   |

---

## 1 Introdução

### 1.1 Finalidade
Este documento tem como finalidade descrever a arquitetura de software do projeto Vitra, uma aplicação movél. A arquitetura descrita aqui serve serve como referência para orientar a equipe ao longo do projeto, servindo também como referência para os interessados.

### 1.2 Escopo


## 2 Representação da Arquitetura

### 2.1 Padrão arquitetural

A arquitetura do Vitra é baseada no padrão **MVC (Model-View-Controller)**. Considerando as tecnologias escolhidas, o MVC é implementado de forma desaclopada, onde a comunicação entre a View e o Controller ocorre via requisições HTTP (API REST).

A aplicação está está estruturada da segunite maneira:

* **Frontend (View):** Construído com React Native, responsável pela interface do usuário no aplicativo móvel.

* **Backend (Model e Controller):** Desenvolvido em Django (utilizando Django REST Framework), responsável pela lógica da aplicação, autenticação e integração com o banco de dados.

* **Banco de dados (Model):** PostgreSQL, centralizando todas as informações da aplicação.

### 2.2 Diagrama 

