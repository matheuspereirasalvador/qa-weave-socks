# 📂 Inventário de Massa de Dados (Test Data)

**Projeto:** WeaveSocks  
**Versão:** 2.0 (Cobertura Total)  
**Data de Atualização:** 26/01/2026  
**Responsável:** Matheus Pereira Salvador  
**Objetivo:** Fornecer dados padronizados para execução de todos os cenários de teste (CT-001 ao CT-041), garantindo cobertura de fluxos positivos, negativos e de borda.

---

## 1. Estrutura e Regras Gerais

Definições de formato para as entidades principais.

### 1.1 Identidade (Auth)
> **Regra Global:** Conforme diretriz de 16/07/2025, `username` e `password` devem ter **máximo de 10 caracteres**. A senha exige 1 especial e 1 número.

| Campo | Chave (Key) | Formato/Restrição | Exemplo Válido |
| :--- | :--- | :--- | :--- |
| **Username** | `username` | Alfanumérico, Máx 10 chars. | `UserTop10` |
| **Nome** | `firstName` | Texto, sem símbolos. | `Ana` |
| **Sobrenome** | `lastName` | Texto, sem símbolos. | `Souza` |
| **E-mail** | `email` | RFC 5322. | `ana@ws.com` |
| **Senha** | `password` | Min 8, Máx 10 chars, Complexa. | `A1@bcdef9` |

### 1.2 Catálogo & Pedido

| Campo | Descrição | Exemplo |
| :--- | :--- | :--- |
| **Qtd Item** | Quantidade no carrinho. | `1` (Válido), `0` (Inválido) |
| **Valor Total** | Valor final do carrinho. | `> $100.00` (Para Antifraude) |

---

## 2. Conjuntos de Dados (Personas)

Utilize os perfis abaixo conforme o **Caso de Teste (CT)** indicado.

### 👤 Perfil A: Caminho Feliz (Standard User)
> **Cobertura:** CT-001, CT-019, CT-020, CT-021, CT-023, CT-024, CT-025, CT-026, CT-028, CT-029, CT-033, CT-036, CT-037.

Use este perfil para fluxos onde o objetivo é o sucesso da operação.

**Cadastro & Login:**
- **Username:** `WayraUser` (9 chars - OK)
- **First Name:** `Wayra`
- **Last Name:** `Lotonies`
- **Email:** `wayra.lotonies@weavesocks.com`
- **Password:** `W@yra123` (8 chars, 1 num, 1 spec - OK)

**Endereço (Shipping):**
- **Street:** `Rua das Flores`
- **Number:** `100`
- **City:** `Curitiba`
- **Zip:** `80000-000`
- **Country:** `Brazil`

**Pagamento:**
- **Card:** `4242 4242 4242 4242` (Visa Test)
- **Expires:** `12/30`
- **CCV:** `123`

---

### 👤 Perfil B: Dados Inválidos (Formato & Segurança)
> **Cobertura:** CT-002, CT-005, CT-006, CT-007, CT-008, CT-009, CT-034, CT-038.

Use este perfil para provocar erros de validação de campo.

| Campo Alvo | Dado de Teste | Motivo da Falha | CT Vinculado |
| :--- | :--- | :--- | :--- |
| **Campos Gerais** | `(vazio)` ou ` ` (espaço) | Campo Obrigatório | CT-002 |
| **Nome/Sobrenome** | `W@yra!`, `L#toni$s` | Caracteres Especiais | CT-005 |
| **E-mail** | `wayra.com`, `user@domain` | Formato Inválido | CT-006 |
| **Senha** | `MinhaSenhaMuitoLonga123!` | > 10 Caracteres (Regra Custom) | CT-007 |
| **Senha** | `WayraUser1!` | Contém parte do Username | CT-009 |
| **Confirmar Senha**| `SenhaDiferente1!` | Divergência | CT-008 |
| **Endereço** | `(vazio)` nos campos obrigatórios | Endereço Inválido | CT-034 |
| **Cartão** | `1234 5678` (Incompleto) | Formato Inválido | CT-038 |

---

### 👤 Perfil C: Teste de Limites (Boundary & Business)
> **Cobertura:** CT-004, CT-030, CT-039, CT-041.

Use para testar fronteiras matemáticas e datas.

| Contexto | Campo | Dado de Teste | Resultado Esperado | CT |
| :--- | :--- | :--- | :--- | :--- |
| **Cadastro** | Nome | `J` (1 char) ou `Ana Beatriz de Oliveira...` (+40) | Erro de Limite | CT-004 |
| **Carrinho** | Quantidade | `0`, `-1`, `-100` | Erro "Valor Inválido" | CT-030 |
| **Pagamento** | Validade | `01/20` (Data Passada) | Cartão Vencido | CT-039 |
| **Antifraude** | Total Carrinho | Adicionar 6x item "Holy" (> $100) | Flag "Análise de Risco" | CT-041 |

---

### 👤 Perfil D: Cenários de Estado (Stateful)
> **Cobertura:** CT-003, CT-013, CT-014, CT-016, CT-022.

Estes testes dependem do estado prévio do banco de dados ou do sistema.

**1. Usuário Duplicado (CT-003):**
* **Ação:** Tentar cadastrar novamente o e-mail do Perfil A (`wayra.lotonies@weavesocks.com`).
* **Resultado:** Erro "E-mail já cadastrado".

**2. Bloqueio de Conta (CT-013):**
* **Dado:** Usuário `WayraUser`.
* **Ação:** Errar a senha 5 vezes consecutivas.
* **Estado Final:** Conta Bloqueada.

**3. Produto Sem Estoque (CT-022):**
* **Produto Alvo:** "Holy Socks" (Configurar no DB `stock: 0`).
* **Ação:** Tentar adicionar ao carrinho.

**4. Token Expirado (CT-016):**
* **Dado:** Código OTP recebido no e-mail.
* **Ação:** Aguardar 16 minutos antes de inserir.

---

## 3. Matriz de Produtos para Teste

Para uso nos testes de Catálogo (CT-019 a CT-024).

| Produto (Nome) | Tags (Categorias) | Preço | Estado Estoque | Uso Principal |
| :--- | :--- | :--- | :--- | :--- |
| **Holy Socks** | `sport`, `formal` | $99.99 | **0 (Sem Estoque)** | Testar validação de estoque (CT-022) |
| **Colourful** | `blue`, `brown` | $18.00 | 100+ | Teste de Filtro (CT-020, CT-024) |
| **Super Sport** | `sport` | $15.00 | 100+ | Teste de Compra Padrão |

---

## 4. Script de Geração (JSON Faker)

Exemplo para automação respeitando a regra de **max 10 chars**:

```json
{
  "username": "User#{randomNumber(3)}", 
  "firstName": "AutoTest",
  "lastName": "Bot",
  "email": "auto.#{timestamp}@ws.com",
  "password": "T!#{randomNumber(4)}a",
  "items": [
    { "productId": "holy_socks_id", "quantity": 1 }
  ]
}
```