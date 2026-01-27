## 🧪 CT-009: Login com dados válidos (positivo)
**Tipo:** Funcional, Smoke, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RF-LOG-01
**ID do Jira:** 
**BUG:** Não
### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. É necessário ter uma conta já cadastrada no site

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Login" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para login foram exibidos | - | ✅ |
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123 | ✅| 
| 3 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 319174A@a  | ✅|
| 4 | Clicar no botão "Log in" | Quando clicar no botão , ele deve entrar na conta  |  O login foi realizado com sucesso | - | ✅ |

---

## 🧪 CT-010: Login com dados que não pertencem a nenhuma conta (negativo)

**Tipo:** Funcional, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RF-LOG-01
**ID do Jira:** 
**BUG:** Não
### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Login" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para login foram exibidos | - | ✅ |
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: aaaaaa | ✅| 
| 3 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: aaaaaa | ✅|
| 4 | Clicar no botão "Log in" | Quando clicar no botão , ele deve ser impedido de criar a conta  | O login foi impedido | - | ✅ |

---
 Buscar dados pela API em busca de informações confidenciais (negativo)

---
Realizar login pela API e verificar se o retorno é válido (positivo)

---

## 🧪 CT-013: Tentar logar 5 vezes errando somente a senha e na 6º vez logar dados corretos (negativo)
**Tipo:** Funcional, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RN-LOG-03
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. É necessário ter uma conta já cadastrada no site

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Login" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para login foram exibidos | - | ✅ |
| 2 | Preencher o campo "Username" com dados incorretos | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123 | ✅| 
| 3 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 319174A@a  | ✅|
| 4 | Clicar no botão "Log in" | Quando clicar no botão , ele deve ser impedido de entrar |  O login foi impedido | - | ✅ |
| 5 | Refazer os passos 1,2,3 e 4 mais quatro vezes | Ele deve ser impedido de entrar nas quatro vezes e deve exibir uma mensagem dizendo que o login foi bloqueado | Não exibiu mensagem informando o bloqueio do login  | - | ✅ |
| 5 | Clicar no botão "Log in" | Quando clicar no botão , ele deve ser impedido de entrar e exibir a mensagem "O usuário está bloqueado" | O login não foi bloqueado e a mensagem não foi exibida  | - | ✅ |

---
## 🧪 CT-014: Tentar logar com a conta em status de confirmação de e-mail (negativo)
**Tipo:** Funcional, Regressivo
**Prioridade:** Alta
**História Vinculada:** RN-LOG-04
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. É necessário ter uma conta já cadastrada no site e em confirmação de e-mail

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Login" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para login foram exibidos | - | ✅ |
| 2 | Preencher o campo "Username" com dados incorretos | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123 | ✅| 
| 3 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 319174A@a  | ✅|
| 4 | Clicar no botão "Log in" | Quando clicar no botão , ele deve ser impedido de entrar e informar que o motivo é que o e-mail não foi confirmado|  | - |  |

---

## 🧪 CT-015: Verificar se o código de confirmação de e-mail foi recebido com sucesso (positivo)
**Tipo:** Funcional, Regressivo, Smoke
**Prioridade:** Alta
**História Vinculada:** RN-LOG-05
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. É necessário ter uma conta já cadastrada no site e em confirmação de e-mail

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Olhar no e-mail e clicar no link/copiar o código recebido e colar no campo que o pede | Receber um link que leva até a página do site já logado e um código que se colar na página permita fazer o login   |  |  | ❌ |
| 2 | Clicar no botão "Login" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para login foram exibidos | - | ✅ |
| 3 | Preencher o campo "Username" com dados incorretos | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123 | ✅| 
| 4 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 319174A@a  | ✅|
| 5 | Clicar no botão "Log in" | O sistema deve permitir o login  |  | - |  |

---

## 🧪 CT-016: Esperar 16 minutos e tentar confirmar o e-mail pelo código recebido (negativo)
**Tipo:** Funcional, Regressivo
**Prioridade:** Alta
**História Vinculada:** RN-LOG-06
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. É necessário ter uma conta já cadastrada no site e em confirmação de e-mail

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Olhar no e-mail, esperar 16 minutos e clicar no link/copiar o código recebido e colar no campo que o pede | Receber um link que leva até a página do site já logado e um código que se colar na página permita fazer o login |  |  | ❌ |
| 2 | Clicar no botão "Login" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para login foram exibidos | - | ✅ |
| 3 | Preencher o campo "Username" com dados incorretos | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123 | ✅| 
| 4 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 319174A@a  | ✅|
| 5 | Clicar no botão "Log in" | O sistema deve bloquear o login e informar que o código expirou  |  | - |  |

---

## 🧪 CT-017: Clicar no botão "Reenviar código" mais de uma vez em um intervalo de 60 segundos (negativo)
**Tipo:** Funcional, Regressivo
**Prioridade:** Alta
**História Vinculada:** RN-LOG-07
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. É necessário ter uma conta já cadastrada no site e em confirmação de e-mail

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Reenviar código" várias vezes em menos de um minuto | Não deve permitir clicar mais deu uma vez sem o intervalo de 60 segundos  |  |  | ❌ |
| 2 | Clicar no botão "Login" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para login foram exibidos | - | ✅ |
| 3 | Preencher o campo "Username" com dados incorretos | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123 | ✅| 
| 4 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 319174A@a  | ✅|
| 5 | Clicar no botão "Log in" | O sistema deve bloquear o login e informar que o código expirou  |  | - |  |

---
## 🧪 CT-018: Tentar enviar o código incorreto 3 vezes e na 4º vez enviar o correto (negativo)
**Tipo:** Funcional, Regressivo
**Prioridade:** Alta
**História Vinculada:** RN-LOG-08
**ID do Jira:** 
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. É necessário ter uma conta já cadastrada no site e em confirmação de e-mail

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Olhar no e-mail e copiar o código recebido e colocar um código errado no campo que o pede | Receber um link que leva até a página do site já logado e um código que se colar na página permita fazer o login   |  |  | ❌ |
| 2 | Repetir o passo 1 três vezes | Deve apontar que o código está incorreto   |  |  | ❌ |
| 3 | Olhar no e-mail e copiar o código recebido e colocar o código no campo que o pede | O login no site deve ser bloqueado e o motivo informado deve ser excesso de tentativas inválidas e deve oferecer a solicitação de um novo código  |  |  | ❌ |
| 4 | Clicar no botão "Login" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para login foram exibidos | - | ✅ |
| 5 | Preencher o campo "Username" com dados incorretos | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123 | ✅| 
| 6 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 319174A@a  | ✅|
| 7 | Clicar no botão "Log in" | O sistema deve permitir o login  |  | - |  |
---



