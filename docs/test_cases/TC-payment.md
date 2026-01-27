# 📂 Cenário: 

> **Descrição:** 
> **Responsável:** Matheus

---

## 🧪 CT-037: Cadastro de forma de pagamento feito com cartão válido (positivo)

**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RF-PAG-01
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
| 1 | Preencher os campos de "Payment" com dados válidos | Os campos devem permitir a escrita | | - |  |
| 2 | Clicar em "Update" | O cadastro do cartão deve ser permitido | | - |  |

---

## 🧪 CT-038: Cadastro de forma de pagamento feito com cartão inválido (negativo)

**Tipo:** Funcional, Regressivo, Automatiado
**Prioridade:** Alta
**História Vinculada:** RF-PAG-01
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
| 1 | Preencher os campos de "Payment" com dados inválidos | Os campos devem permitir a escrita | | - |  |
| 2 | Clicar em "Update" | O cadastro do cartão deve ser impedido | | - |  |

---

## 🧪 CT-039:  Cadastro de forma de pagamento feito com cartao com data de válidade anterior ao dia atual (negativo)
**Tipo:** Funcional, Regressivo, Automatiado
**Prioridade:** Alta
**História Vinculada:** RN-PAG-01
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
| 1 | Preencher os campos de "Payment" com data de validade anterior ao dia atual | Os campos devem permitir a escrita | | - |  |
| 2 | Clicar em "Update" | O cadastro do cartão deve ser impedido | | - |  |

---

## 🧪 CT-040:  Clicar duas vezes rápido na hora do pagamento (negativo)

**Tipo:** Funcional, Regressivo, Automatiado
**Prioridade:** Alta
**História Vinculada:** RN-PAG-03
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
| 2 | Clicar em "Proceed to checkout" duas vezes seguidas | A compra deve ser feita (e cobrada) somente uma vez| | - |  |

---

## 🧪 CT-041:  Realizar compra com valor superior a $ 100,00 (positivo)

**Tipo:** Funcional, Regressivo, Automatiado
**Prioridade:** Alta
**História Vinculada:** RN-PAG-02
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário deve estar logado no site
3. Precisa ter produtos no carrinho que somem mais de 100 dólares
4. Estar no carrinho

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Preencher os campos de "Shipping Address" e "Payment" com dados válidos | Os campos devem permitir a escrita | | - |  |
| 2 | Clicar em "Proceed to checkout" duas vezes seguidas | O sistema deve fazer uma verificação para dizer se o cartão é válido| | - |  |

---
