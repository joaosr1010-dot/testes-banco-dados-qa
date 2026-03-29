# 🐞 Relatórios de Bugs

---

## 🐞 BUG01 - Aceitação de email inválido

**Descrição:**
Sistema permite cadastro de usuário com email fora do padrão.

**Passos para reproduzir:**

1. Inserir usuário com email inválido
2. Executar query de inserção

**Resultado esperado:**
Sistema deveria bloquear o cadastro.

**Resultado obtido:**
Cadastro realizado com sucesso.

**Severidade:** Média

---

## 🐞 BUG02 - Permite email nulo

**Descrição:**
Sistema permite cadastro de usuário sem email.

**Resultado esperado:**
Campo deveria ser obrigatório.

**Resultado obtido:**
Registro inserido com valor NULL.

**Severidade:** Média

---

## 🐞 BUG03 - Permite idade negativa

**Descrição:**
Sistema aceita valores inválidos para idade.

**Resultado esperado:**
Idade deve ser maior que zero.

**Resultado obtido:**
Valor negativo inserido.

**Severidade:** Alta

---

## 🐞 BUG04 - Pedido associado a usuário inexistente

**Descrição:**
Sistema permite criação de pedido com usuário inexistente.

**Passos para reproduzir:**

1. Inserir pedido com usuario_id inexistente (ex: 999)

**Resultado esperado:**
Sistema deveria impedir inserção.

**Resultado obtido:**
Pedido inserido com sucesso.

**Severidade:** Alta

---

# ✅ Validações do Sistema

---

## ✅ VAL01 - Restrição de chave primária (PRIMARY KEY)

**Descrição:**
Sistema impede inserção de registros com ID duplicado.

**Passos para reproduzir:**

1. Inserir um usuário com ID já existente

**Resultado esperado:**
Sistema deve impedir duplicação de ID.

**Resultado obtido:**
Erro de constraint exibido (UNIQUE constraint failed).

**Status:** Funcionando corretamente

---
