# 📊 Projeto de Testes em Banco de Dados (SQLite)

---

## 🎯 Objetivo do projeto

Simular testes em banco de dados utilizando SQL, validando:
- Inserção de dados
- Consultas
- Integridade das informações

---

## 📌 Sobre o projeto

Este projeto tem como objetivo praticar testes em banco de dados utilizando SQLite, simulando cenários reais de validação de dados e identificação de inconsistências.

Os testes foram realizados com base em consultas SQL (SELECT), validando o estado final dos dados armazenados no banco.

---

## 🧠 Habilidades demonstradas

* Criação e manipulação de tabelas
* Escrita de queries SQL (SELECT, WHERE, JOIN)
* Validação de dados
* Identificação de inconsistências
* Documentação de testes (test cases)
* Registro de bugs

---

## 🗂 Estrutura do banco

### Tabela: usuarios

* id (chave primária)
* nome
* email
* idade

### Tabela: pedidos

* id (chave primária)
* usuario_id
* produto
* valor

---

## 🔗 Relacionamento entre tabelas

A tabela `pedidos` se relaciona com a tabela `usuarios` através do campo `usuario_id`, permitindo associar cada pedido a um usuário.

---

## 🧪 Casos de teste

Os testes realizados incluem:

* Validação de usuário existente
* Identificação de email inválido
* Identificação de email nulo
* Identificação de idade inválida
* Listagem de usuários
* Relacionamento entre tabelas (JOIN)
* Identificação de pedidos com usuário inexistente

📄 Detalhes completos em: `test-cases.md`

---

## 🐞 Bugs encontrados

Durante os testes, foram identificados os seguintes problemas:

* Permissão de email inválido
* Permissão de email nulo
* Permissão de idade negativa
* Pedido associado a usuário inexistente

📄 Detalhes completos em: `bug-report.md`

---

## 📸 Evidências

As evidências dos testes estão disponíveis na pasta:

📁 `evidencias/`

Contendo prints das execuções das queries utilizadas nos testes.

---

## ⚙️ Observações técnicas

* Os testes foram validados por meio de consultas SELECT, analisando o estado final dos dados armazenados no banco.
* A abordagem utilizada permitiu identificar dados inconsistentes e ausência de validações na base.

---

## 🚀 Possíveis melhorias

* Implementação de validações nos campos (email, idade)
  → Para evitar o armazenamento de dados inválidos.

* Uso de constraints (NOT NULL, CHECK)
  → Para garantir regras básicas de integridade diretamente no banco.

* Implementação de chave estrangeira (FOREIGN KEY)
  → Para impedir a criação de registros relacionados a dados inexistentes.

* Melhor tratamento de integridade dos dados
  → Para garantir consistência e confiabilidade nas informações armazenadas.

---

## 🛠 Tecnologias utilizadas

* SQLite
* SQL

---

## 🎯 Objetivo profissional

Este projeto foi desenvolvido com foco na prática de testes de banco de dados, visando evolução na área de Quality Assurance (QA), com aplicação de conceitos reais de validação e análise de dados.

---
