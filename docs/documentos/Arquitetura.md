# Documento de Arquitetura

## Histórico de Versão

| Data       | Versão | Descrição                                | Autor(es)      |
| ---------- | ------ | ---------------------------------------- | -------------- |
| 1/11/2025 | 1.0    | Criação do documento de arquitetura      | Pedro Vargas, Thiago Gomes   |

---

## 1 Introdução

### 1.1 Finalidade
Este documento tem como finalidade descrever a arquitetura de software do projeto Vitra, uma aplicação movél. A arquitetura descrita aqui serve serve como referência para orientar a equipe ao longo do projeto, servindo também como referência para os interessados.

### 1.2 Escopo
O **Vitra** é um aplicativo mobile desenvolvido por estudantes da **Universidade de Brasília (UnB)**, com o objetivo de servir como uma **vitrine de projetos** voltada para **pesquisadores, colaboradores e empresas**. Este documento descreve os aspectos técnicos essenciais da arquitetura do sistema, abrangendo tanto o **Frontend** quanto o **Microsserviço API**.

## 2 Representação da Arquitetura

### 2.1 Padrão Arquitetural

A arquitetura do **Vitra** adota uma abordagem baseada em **microsserviços**, composta por dois principais componentes independentes:  

- **Frontend:** Responsável pela interface e experiência do usuário no aplicativo móvel.  
- **Microsserviço API:** Responsável pela camada de backend e pela disponibilização dos serviços da aplicação.  

### 2.2 Frontend

O **Frontend**, desenvolvido em **React Native**, atua como cliente da API REST. Ele representa a camada **View** da arquitetura global, sendo responsável por consumir os serviços oferecidos pelo backend e apresentar as informações de forma interativa ao usuário final.


### 2.3 Microsserviço API

No **Microsserviço API**, foi adotado o padrão arquitetural **MVC (Model-View-Controller)**, implementado por meio do **Django REST Framework**. Nesse modelo, as responsabilidades são bem definidas e desacopladas:

- **Model:** Representa a camada de dados e as regras de negócio, sendo responsável pela comunicação com o banco de dados **PostgreSQL**, que centraliza e persiste todas as informações da aplicação.  
- **View:** Corresponde às *views* do Django REST Framework, que expõem os dados e funcionalidades do sistema através de endpoints da API REST.  
- **Controller:** É representado pelos *serializers* e *viewsets*, que processam as requisições, aplicam regras de validação e intermediam a comunicação entre as views e os models.

Dessa forma, a comunicação entre o microsserviço e o frontend ocorre por meio de **requisições HTTP**, garantindo um **baixo acoplamento** entre as partes e facilitando a **escalabilidade**, **manutenção** e **evolução independente** de cada componente.


### 2.4 Diagrama 

