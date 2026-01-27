# 📂 Cenário: Pedido

> **Descrição:** 
> **Responsável:** Matheus

---

## 🧪 CT-033: Fazer pedido com dados válidos (positivo)

**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RF-PED-01
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário deve estar logado no site
3. Precisa ter um produto no carrinho
4. Estar no carrinho

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Preencher os campos de "Shipping Address" e "Payment" com dados válidos | Os campos devem permitir a escrita | | - |  |
| 2 | Clicar em "Proceed to checkout" | A compra deve ser efetivada com sucesso | | - |  |

---

## 🧪 CT-034: Fazer pedidos com endereço inválido (negativo)

**Tipo:** Funcional, Regressivo, Automatizado
**Prioridade:** Alta
**História Vinculada:** RN-PED-01
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário deve estar logado no site
3. Precisa ter um produto no carrinho
4. Estar no carrinho

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Preencher os campos de "Payment" com dados válidos e os de "Shipping Address" com endereço inválido | Os campos devem permitir a escrita | | - |  |
| 2 | Clicar em "Proceed to checkout" | A compra deve ser impedida e uma mensagem de erro deve ser exibida  | | - |  |

---

## 🧪 CT-035: Verificar se a alteração de preço quando o pedido é criado, não afeta a compra (positivo)

**Tipo:** Funcional, Regressivo, Automatizado
**Prioridade:** Alta
**História Vinculada:** RN-PED-02
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário deve estar logado no site
3. Precisa ter um produto no carrinho
4. Estar no carrinho

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Preencher os campos de "Payment" com dados válidos e os de "Shipping Address" com endereço inválido | Os campos devem permitir a escrita  | | - |  |
| 2 | O preço de um dos itens comprados sofreu alterações  | O preço dos itens que já vão ser comprados não sofram alteração junto | | - |  |
| 2 | Clicar em "Proceed to checkout" | A compra deve ser efetivada com sucesso | | - |  |

---

## 🧪 CT-036: Verificar se o carrinho foi limpo após a compra ser efetuada com sucesso (positivo)

**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RN-PED-03
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário deve estar logado no site
3. Precisa ter um produto no carrinho
4. Estar no carrinho

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Preencher os campos de "Shipping Address" e "Payment" com dados válidos | Os campos devem permitir a escrita | | - |  |
| 2 | Clicar em "Proceed to checkout" | A compra deve ser efetivada com sucesso | | - |  |
| 3 | Retornar ao carrinho e verificar se os itens foram removidos |O carrinho deve estar limpo (vazio) | | - |  |
---