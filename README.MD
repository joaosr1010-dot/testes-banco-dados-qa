# 📊 Projeto de Testes em Banco de Dados (SQLite)

---

## 🎯 Objetivo do projeto

Simular testes em banco de dados utilizando SQL, com foco na:

* Validação de dados
* Execução de consultas
* Identificação de inconsistências
* Verificação de integridade entre tabelas

---

## 📌 Sobre o projeto

Este projeto tem como objetivo praticar testes em banco de dados utilizando SQLite, simulando cenários reais de validação e análise de dados.

Os testes foram realizados por meio de consultas SQL (SELECT), permitindo validar o estado final das informações armazenadas no banco.

---

## 🧠 Habilidades demonstradas

* Criação e manipulação de tabelas
* Escrita de queries SQL (SELECT, WHERE, JOIN)
* Validação de dados
* Identificação de inconsistências
* Documentação de testes (casos de teste)
* Registro de bugs

---

## 🗄️ Estrutura do banco de dados

O projeto utiliza duas tabelas principais:

### Tabela: usuarios

```sql
CREATE TABLE usuarios (
  id INTEGER PRIMARY KEY,
  nome TEXT,
  email TEXT,
  idade INTEGER
);
```

### Tabela: pedidos

```sql
CREATE TABLE pedidos (
  id INTEGER PRIMARY KEY,
  usuario_id INTEGER,
  produto TEXT,
  valor REAL
);
```

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

📄 Detalhes completos em: `casos-de-teste.md`

---

## 🐞 Bugs encontrados

Durante os testes, foram identificados os seguintes problemas:

* Permissão de email inválido
* Permissão de email nulo
* Permissão de idade negativa
* Pedido associado a usuário inexistente

📄 Detalhes completos em: `relatorio-de-bugs.md`

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

## 🧠 Aprendizados

Durante o desenvolvimento deste projeto, foi possível compreender:

* A importância da validação de dados no banco
* Como consultas SQL podem ser utilizadas para testes
* A necessidade de garantir integridade entre tabelas
* Como documentar testes e evidências de forma estruturada

---

## 🛠 Tecnologias utilizadas

* SQLite
* SQL

---

## 🎯 Objetivo profissional

Este projeto foi desenvolvido com foco na prática de testes de banco de dados, visando evolução na área de Quality Assurance (QA), com aplicação de conceitos reais de validação e análise de dados.

---
