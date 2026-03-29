# 📋 Casos de Teste - Projeto Banco de Dados (SQLite)

---

## 🧪 CT01 - Validar usuário cadastrado

**Query:**
SELECT * FROM usuarios WHERE id = 1;

**Objetivo:**
Verificar se o usuário foi inserido corretamente no banco.

**Resultado esperado:**
O usuário com ID 1 deve existir na base de dados.

**Resultado obtido:**
Usuário encontrado com sucesso.

**Status:** PASSOU

---

## 🧪 CT02 - Validar usuário com email inválido

**Query:**
SELECT * FROM usuarios WHERE email = 'email_invalido';

**Objetivo:**
Verificar se o sistema permite cadastro com email inválido.

**Resultado esperado:**
O sistema não deveria permitir esse tipo de registro.

**Resultado obtido:**
Usuário encontrado com email inválido.

**Status:** FALHOU

---

## 🧪 CT03 - Validar usuário com email nulo

**Query:**
SELECT * FROM usuarios WHERE email IS NULL;

**Objetivo:**
Verificar se o sistema permite cadastro sem email.

**Resultado esperado:**
O sistema não deveria permitir valores nulos.

**Resultado obtido:**
Usuário encontrado com email NULL.

**Status:** FALHOU

---

## 🧪 CT04 - Validar usuário com idade negativa

**Query:**
SELECT * FROM usuarios WHERE idade < 0;

**Objetivo:**
Verificar se o sistema permite idade inválida.

**Resultado esperado:**
O sistema não deveria permitir idade negativa.

**Resultado obtido:**
Usuário encontrado com idade negativa.

**Status:** FALHOU

---

## 🧪 CT05 - Listar todos os usuários

**Query:**
SELECT * FROM usuarios;

**Objetivo:**
Verificar se todos os usuários cadastrados são exibidos.

**Resultado esperado:**
A consulta deve retornar todos os registros da tabela.

**Resultado obtido:**
Lista retornada corretamente.

**Status:** PASSOU

---

## 🧪 CT06 - Listar pedidos com seus respectivos usuários

**Query:**
SELECT usuarios.nome, pedidos.produto
FROM usuarios
JOIN pedidos ON usuarios.id = pedidos.usuario_id;

**Objetivo:**
Verificar o relacionamento entre usuários e pedidos.

**Resultado esperado:**
A consulta deve retornar o nome do usuário e o produto correspondente.

**Resultado obtido:**
Dados retornados corretamente para usuários existentes.

**Status:** PASSOU

---

## 🧪 CT07 - Verificar pedidos com usuário inexistente

**Query:**
SELECT * FROM pedidos WHERE usuario_id = 999;

**Objetivo:**
Identificar pedidos associados a usuários inexistentes.

**Resultado esperado:**
O sistema não deveria permitir esse tipo de registro.

**Resultado obtido:**
Pedido encontrado com usuário inexistente.

**Status:** FALHOU

---

