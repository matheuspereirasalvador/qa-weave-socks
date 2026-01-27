# 📂 Cenário: Registro

> **Descrição:** Garantir que as funcionalidades críticas de registro estejam funcionando perfeitamente 
> **Responsável:** Matheus

---

## 🧪 CT-001: Cadastro realizado com sucesso (positivo)
**Tipo:** Funcional, Smoke, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RF-CAD-01
**ID do Jira:** WSSQ-T1
**BUG:** Sim 
### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Register" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para registro foram exibidos | - | ✅
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123 | ✅| 
| 3 | Preencher o campo "First Name" | O campo deve permitir a escrita |A escrita foi permitida no campo |First Name: Wayra  | ✅|
| 4 | Preencher o campo "Last Name" | O campo deve permitir a escrita |A escrita foi permitida no campo |Last Name: Lotonies | ✅|
| 5 | Preencher o campo "Email" | O campo deve permitir a escrita |A escrita foi permitida no campo |Email: wayralotonies123@gmail.com" | ✅|
| 6 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 319174A@a  | ✅|
| 7 | Clicar no botão "Register" | Quando clicar no botão , ele deve criar a conta  | A conta foi criada com sucesso e o login foi feito logo em seguida  | - | ✅ |
---

## 🧪 CT-002: Cadastro realizado com campos em branco (negativo) 
**Tipo:** Funcional, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RN-CAD-02
**ID do Jira:** WSSQ-T2
**BUG:** 

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. Já deve ter uma conta com o e-mail utilizado cadastrado

### 👣 Roteiro

| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Register" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para registro foram exibidos | - | ✅
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra1234 | ✅| 
| 3 | Preencher o campo "First Name" | O campo deve permitir a escrita |A escrita foi permitida no campo |First Name: Wayra1  | ✅|
| 4 | Preencher o campo "Last Name" | O campo deve permitir a escrita |A escrita foi permitida no campo |Last Name: Lotonies1 | ✅|
| 5 | Preencher o campo "Email" | O campo deve permitir a escrita |A escrita foi permitida no campo |Email: wayralotonies1234@gmail.com" | ✅|
| 6 | Deixar o campo "Password" vazio | O campo deve ficar vazio | O campo ficou vazio |  | ✅|
| 7 | Clicar no botão "Register" | Quando clicar no botão, criação da conta deve ser bloqueada e uma mensagem deve avisar que tem campos em branco| A conta foi criada com sucesso e o login foi feito logo em seguida | - | ❌ |

---

## 🧪 CT-003: Cadastro de dois usuários diferentes com o mesmo e-mail (negativo)
**Tipo:** Funcional, Regressivo, Automatizado
 **Prioridade:** Alta
**História Vinculada:** RN-CAD-01
**ID do Jira:** WSSQ-T3
**BUG:** Sim

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro

| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Register" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para registro foram exibidos | - | ✅
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123451 | ✅| 
| 3 | Preencher o campo "First Name" | O campo deve permitir a escrita |A escrita foi permitida no campo |First Name: Wayra1321  | ✅|
| 4 | Preencher o campo "Last Name" | O campo deve permitir a escrita |A escrita foi permitida no campo |Last Name: Lotonies111 | ✅|
| 5 | Preencher o campo "Email" com um e-mail já existente | O campo deve permitir a escrita |A escrita foi permitida no campo |Email: wayralotonies123@gmail.com" | ✅|
| 6 | Preencher o campo "Password"| O campo deve permitir a escrita | O campo permitiu a escrita | 329214A!b | ✅|
| 7 | Clicar no botão "Register" | Quando clicar no botão, criação da conta deve ser bloqueada e uma mensagem deve avisar que esse e-mail já foi utilizado | A conta foi criada com sucesso e o login foi feito logo em seguida  | - | ❌ |

---

## 🧪 CT-004: Cadastro de usuário com nome e sobrenome de tamanho inválido (negativo)
**Tipo:** Funcional, Regressivo, Automatizado 
**Prioridade:** Alta
**História Vinculada:** RF-CAD-03
**ID do Jira:** WSSQ-T4
**BUG:** Sim
### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual| Dados de teste |  Status | 
| :--- | :--- | :--- | :--- | :--- | :--- 
| 1 | Clicar no botão "Register" | Quando clicar no botão, ele exibirá os campos para preencher | Os campos para registro foram exibidos | - | ✅
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | A escrita foi permitida no campo | Username: Wayra123423 | ✅| 
| 3 | Preencher o campo "First Name" com 2, 40, 20, 1, 41 caracteres | O campo deve permitir a escrita |A escrita foi permitida no campo | First Name: J, Al, Mariana Silva Santos, Guilherme de Albuquerque Cavalcanti Souza, Ana Beatriz de Oliveira Figueiredo da Rosa  | ✅|
| 4 | Preencher o campo "Last Name" | O campo deve permitir a escrita |A escrita foi permitida no campo |Last Name: Lotonies | ✅|
| 5 | Preencher o campo "Email" | O campo deve permitir a escrita |A escrita foi permitida no campo |Email: wayralotonies11223@gmail.com" | ✅|
| 6 | Preencher o campo "Password" | O campo deve permitir a escrita |A escrita foi permitida no campo |Password: 31219174A@a  | ✅|
| 7 | Clicar no botão "Register" | Quando clicar no botão , ele deve impedir o cadastro e informar que o nome é muito grande ou muito pequeno  | A conta foi criada com sucesso e o login foi feito logo em seguida  | - | ❌  |

---
## 🧪 CT-005: Cadastro de usuário com nome e sobrenome que contém caracteres especiais (negativo)
**Tipo:** Funcional, Regressivo, Automatizado
**Prioridade:** Média
**História Vinculada:** RN-CAD-04
**ID do Jira:** WSSQ-T5
**BUG:** Sim

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual | Dados de teste | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Clicar no botão "Register" | Os campos para registro devem ser exibidos | Os campos foram exibidos | - | ✅ |
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita (max 10 chars) | Escrita permitida | Username: UserTst05 | ✅ |
| 3 | Preencher o campo "First Name" com caracteres especiais | O campo deve permitir a escrita | Escrita permitida | First Name: W@yra! | ✅ |
| 4 | Preencher o campo "Last Name" com caracteres especiais | O campo deve permitir a escrita | Escrita permitida | Last Name: L#toni$s | ✅ |
| 5 | Preencher o campo "Email" | O campo deve permitir a escrita | Escrita permitida | Email: teste05@gmail.com | ✅ |
| 6 | Preencher o campo "Password" | O campo deve permitir a escrita | Escrita permitida | Password: 123456*Ab | ✅ |
| 7 | Clicar no botão "Register" | O sistema deve bloquear o cadastro informando que o nome não deve conter caracteres especiais | A conta foi criada com sucesso | - | ❌ |

---

## 🧪 CT-006: Cadastro de usuário com e-mail inválido (negativo)
**Tipo:** Funcional, Regressivo, Automatizado
**Prioridade:** Alta
**História Vinculada:** RN-CAD-05
**ID do Jira:** 
**BUG:** Sim

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual | Dados de teste | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Clicar no botão "Register" | Os campos para registro devem ser exibidos | Os campos foram exibidos | - | ✅ |
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | Escrita permitida | Username: UserTst06 | ✅ |
| 3 | Preencher o campo "First Name" | O campo deve permitir a escrita | Escrita permitida | First Name: Wayra | ✅ |
| 4 | Preencher o campo "Last Name" | O campo deve permitir a escrita | Escrita permitida | Last Name: Lotonies | ✅ |
| 5 | Preencher o campo "Email" sem o caractere '@' ou sem domínio | O campo deve permitir a escrita | Escrita permitida | Email: wayralotonies.com | ✅ |
| 6 | Preencher o campo "Password" | O campo deve permitir a escrita | Escrita permitida | Password: Pass123!@ | ✅ |
| 7 | Clicar no botão "Register" | O sistema deve **bloquear** o cadastro e solicitar um e-mail válido | A conta foi criada com sucesso | - | ❌ |

---

## 🧪 CT-007: Cadastro de usuário com nome, sobrenome e e-mail válidos e senha inválida (negativo)
**Tipo:** Funcional, Regressivo, Automatizado
**Prioridade:** Alta
**História Vinculada:** RN-CAD-06
**ID do Jira:** 
**BUG:** Sim

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks


### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual | Dados de teste | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Clicar no botão "Register" | Os campos para registro devem ser exibidos | Os campos foram exibidos | - | ✅ |
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | Escrita permitida | Username: UserTst07 | ✅ |
| 3 | Preencher o campo "First Name" | O campo deve permitir a escrita | Escrita permitida | First Name: Wayra | ✅ |
| 4 | Preencher o campo "Last Name" | O campo deve permitir a escrita | Escrita permitida | Last Name: Lotonies | ✅ |
| 5 | Preencher o campo "Email" | O campo deve permitir a escrita | Escrita permitida | Email: teste07@gmail.com | ✅ |
| 6 | Preencher o campo "Password" com mais de 10 caracteres | O campo deve permitir a escrita | Escrita permitida | Password: Minh (19 chars) | ✅ |
| 7 | Clicar no botão "Register" | O sistema deve **bloquear** o cadastro (Senha > 10 caracteres) | A conta foi criada com sucesso ignorando o limite | - | ❌ |

---

## 🧪 CT-008: Cadastro de usuário com campo Senha diferente de campo Confirmar Senha (negativo)
**Tipo:** Funcional, Regressivo
**Prioridade:** Alta
**História Vinculada:** RF-CAD-05
**ID do Jira:** **BUG:** Sim

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks
2. O formulário deve possuir o campo "Confirm Password"

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual | Dados de teste | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Clicar no botão "Register" | Os campos para registro devem ser exibidos | Os campos foram exibidos | - | ✅ |
| 2 | Preencher os dados pessoais (User, Nome, Email) | Os campos devem permitir a escrita | Escrita permitida | User: UserTst08 | ✅ |
| 3 | Preencher o campo "Password" | O campo deve permitir a escrita | Escrita permitida | Password: Senha1! | ✅ |
| 4 | Preencher o campo "Confirm Password" com valor diferente | O campo deve permitir a escrita | Escrita permitida | Confirm Pass: Senha2@ | ✅ |
| 5 | Clicar no botão "Register" | O sistema deve **bloquear** o cadastro informando que as senhas não conferem | O sistema criou a conta considerando a primeira senha | - | ❌ |

---

## 🧪 CT-009: Cadastro de usuário com senha sendo parte do nome ou e-mail (negativo)
**Tipo:** Funcional, Segurança
**Prioridade:** Média
**História Vinculada:** RN-CAD-08
**ID do Jira:** 
**BUG:** Sim

### 🛠️ Pré-condições
1. O visitante precisa estar no site WeaveSocks

### 👣 Roteiro
| Passo | Ação | Resultado Esperado | Resultado Atual | Dados de teste | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Clicar no botão "Register" | Os campos para registro devem ser exibidos | Os campos foram exibidos | - | ✅ |
| 2 | Preencher o campo "Username" | O campo deve permitir a escrita | Escrita permitida | Username: WayraUser | ✅ |
| 3 | Preencher o campo "Email" | O campo deve permitir a escrita | Escrita permitida | Email: wayra@gmail.com | ✅ |
| 4 | Preencher o campo "Password" contendo o Username | O campo deve permitir a escrita | Escrita permitida | Password: WayraUser1! | ✅ |
| 5 | Clicar no botão "Register" | O sistema deve **bloquear** por política de segurança (senha fraca/previsível) | A conta foi criada com sucesso | - | ❌ |