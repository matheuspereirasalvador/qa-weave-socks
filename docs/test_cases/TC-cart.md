# 📂 Cenário: Carrinho

> **Descrição:** 
> **Responsável:** Matheus

---

## 🧪 CT-025: Adicionar item ao carrinho (positivo)
**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RF-CAR-01
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Escolher um produto e clicar em "Add to cart" | Quando clicar no botão, ele deve adicionar o item escolhido ao carrinho || Produto: Holy | ✅ |

---

## 🧪 CT-026: Remover item do carrinho (positivo)
**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RF-CAR-02
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O carrinho já deve ter um produto

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Clicar no botão do carrinho | Quando clicar no botão, ele deve abrir uma página que contenha o conteúdo do carrinho, bem como os botões para remover e adicionar produtos|| Produto: Holy | ✅ |
| 3 | Clicar no botão de remover o produto | Quando clicar no botão, ele deve remover o produto do carrinho|| Produto: Holy | ✅ |

---

## 🧪 CT-027: "Aumentar, Diminuir" a quantidade de um item (positivo)
**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RF-CAR-02
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O carrinho já deve ter um produto

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Clicar no botão do carrinho | Quando clicar no botão, ele deve abrir uma página que contenha o conteúdo do carrinho, bem como os botões para remover e adicionar produtos|| Produto: Holy | ✅ |
| 3 | Clicar no botão de aumentar/diminuir a quantidade do produto | Quando clicar no botão, a quantidade deve ser alterada, aumentando ou diminuindo em 1|| Produto: Holy |  |

---

## 🧪 CT-028: Alterar a quantidade de um item (positivo)

**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RF-CAR-02
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O carrinho já deve ter um produto

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Clicar no botão do carrinho | Quando clicar no botão, ele deve abrir uma página que contenha o conteúdo do carrinho, bem como os botões para remover e adicionar produtos|| Produto: Holy | ✅ |
| 3 | Clicar no campo de alterar a quantidade de itens do produto e escrever algum valor e teclar enter | A quantidade de itens do carrinho deve mudar para a quantidade informada bem como seu preço|| Produto: Holy |  |

---

## 🧪 CT-029: Adicionar itens ao carrinho enquanto não estiver logado e depois realizar o login (positivo)

**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RN-CAR-01
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Escolher um produto e clicar em "Add to cart" | Quando clicar no botão, ele deve adicionar o item escolhido ao carrinho || Produto: Holy | ✅ |
| 3 | Logar no sistema | Quando realizar o login o carrinho deverá manter o item que estava nele enquanto anônimo | | Produto: Holy |  |

---

## 🧪 CT-030: Adicionar "0, -2" itens ao carrinho (negativo)

**Tipo:** Funcional, Regressivo, Automatizado
**Prioridade:** Alta
**História Vinculada:** RN-CAR-02
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Escolher um produto e clicar em "Add to cart" | Quando clicar no botão, ele deve adicionar o item escolhido ao carrinho || Produto: Holy | ✅ |
| 3 | Clicar no campo de alterar a quantidade de itens do produto e escrever o valor de 0 ou algum valor negativo | Deve dar um erro e exibir uma mensagem informativa "valor inválido" || Produto: Holy Dados de teste: 0, -3 |  |

---

## 🧪 CT-031: Deixar um item no carrinho por 24 horas enquanto está deslogado (negativo)

**Tipo:** Funcional, Regressivo
**Prioridade:** Alta
**História Vinculada:** RN-CAR-03
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. Precisa ter um produto no carrinho

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Esperar 24 horas e abrir o carrinho | O item deve sumir do carrinho | | - |  |

---

## 🧪 CT-032: Verificar se a mudança de preço é exibida (positivo)

**Tipo:** Funcional, Regressivo
**Prioridade:** Alta
**História Vinculada:** RN-CAR-04
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. Precisa ter um produto no carrinho

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Preço é alterado | O usuário que está com um produto no carrinho deve ser avisado por uma mensagem caso o preço desse produto mudar | | - |  |
