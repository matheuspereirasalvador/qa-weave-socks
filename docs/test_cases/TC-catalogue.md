# 📂 Cenário: Catálogo

> **Descrição:** 
> **Responsável:** Matheus

---

## 🧪 CT-019: Verificar se os itens exibidos no cátalogo contém as informações necessárias (positivo)
**Tipo:** Funcional, Smoke, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RF-CTG-01
**ID do Jira:** 
**BUG:**  
### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário precisa estar logado no site e na página do cátalogo

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅
---

## 🧪 CT-020: Filtrar produtos por categoria (positivo)
**Tipo:** Funcional, Smoke, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RF-CTG-02
**ID do Jira:** 
**BUG:** 
### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário precisa estar logado no site e na página do cátalogo

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Escolher uma categoria do filtro | Quando clicar no botão, ele deve dar um check na caixa e os produtos devem ser filtrados cmo base na categoria escolhida || Categoria: azul | ✅ |

---

## 🧪 CT-021: Abrir detalhes do produto (positivo)
**Tipo:** Funcional, Smoke, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RF-CTG-03
**ID do Jira:** 
**BUG:** 
### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário precisa estar logado no site e na página do cátalogo

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Clicar na imagem ou nome de um produto qualquer | Quando clicar na imagem ou nome de um produto qualquer ele deve exibir suas informações mais detalhadas |  | Produto: Holy | ✅ |

---

## 🧪 CT-022: Tentar adicionar ao carrinho produtos que não possuem itens em estoque (negativo)
**Tipo:** Funcional, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RN-CTG-01
**ID do Jira:** 
**BUG:** 
### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário precisa estar logado no site e na página do cátalogo
3. O produto escolhido para testes deve ser esvaziado no estoque

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Clicar no botão "Adicionar ao Carrinho" de um produto que esteja zerado no estoque | O botão deve estar indisponível para clicar ou fornecer uma mensagem de erro dizendo que não tem estoque desse produto |  | Produto: Holy | ✅ |

---

## 🧪 CT-023: Verificar se o preço do produto na listagem é o mesmo preço quando entra na tela de detalhes do produto (positivo)
**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RN-CTG-02
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário precisa estar logado no site e na página do cátalogo

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Verificar o preço de um produto e clicar na imagem ou nome desse produto | O preço que foi observado antes deve ser o mesmo do que está aparecendo na tela de detalhes |  | Produto: Holy | ✅ |

---

## 🧪 CT-024: Filtrar produtos por duas categorias (positivo)
**Tipo:** Funcional, Regressivo, Automatizado, Smoke
**Prioridade:** Alta
**História Vinculada:** RN-CTG-03
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O usuário precisa estar logado no site e na página do cátalogo

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Catalogue" | Quando clicar no botão, ele exibirá os produtos à venda e suas informações necessárias | Os produtos e as informações foram exibidos | - | ✅ |
| 2 | Escolher duas categorias do filtro | Quando clicar no botão, ele deve dar um check na caixa e os produtos devem ser filtrados como se fosse uma fórmula AND em conjuntos ("sport" e "azul" só aparecer meias esportivas azuis) || Categoria: azul E sport | ✅ |

---