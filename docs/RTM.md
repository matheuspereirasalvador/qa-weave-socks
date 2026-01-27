# Matriz de Rastreabilidade de Requisitos (RTM)

**Projeto:** WeaveSocks
**Versão:** 1.0  
**Data:** 25/01/2026
**Autor:** Matheus Pereira Salvador  
**Status:** Em elaboração  

---

## 1. Objetivo

Este documento tem como objetivo garantir a rastreabilidade completa entre os requisitos do sistema, os cenários de teste, os casos de teste e os defeitos identificados, assegurando que todos os requisitos sejam devidamente validados durante o ciclo de testes.

---

## 2. Estrutura da Rastreabilidade

A matriz relaciona:

- Requisitos Funcionais (RF)
- Requisitos Não Funcionais (RNF)
- Regras de Negócio (RN)
- Casos de Teste
- Tipo de Teste
- Status de Execução
- Defeitos associados

---

## 3. Matriz de Rastreabilidade

### 3.1 Cadastro

| ID Requisito | Descrição do Requisito | Caso(s) de Teste | Tipo de Teste | Status | Defeito |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RF-CAD-01** | O usuário deve poder se cadastrar fornecendo: Nome, Sobrenome, Email e Senha. | CT-001 | Funcional, Smoke, Regressivo, Automatizado | **Passou** | — |
| **RN-CAD-01** | Não é permitido cadastrar dois usuários com o mesmo e-mail. | CT-003 | Funcional, Regressivo, Automatizado | **Falhou** | Sim |
| **RN-CAD-02** | O cadastro não pode ser processado se campos obrigatórios estiverem vazios. | CT-002 | Funcional, Regressivo, Automatizado | **Falhou** | Sim |
| **RN-CAD-03** | Limites de caracteres: Nome/Sobrenome (2-40), Senha (8-100). | CT-004 | Funcional, Regressivo, Automatizado | **Falhou** | Sim |
| **RN-CAD-04** | Nome/Sobrenome não devem aceitar caracteres numéricos ou especiais. | CT-005 | Funcional, Regressivo, Automatizado | **Falhou** | Sim |
| **RN-CAD-05** | E-mail deve ser validado via Regex padrão (RFC 5322). | CT-006 | Funcional, Regressivo, Automatizado | **Falhou** | Sim |
| **RN-CAD-06** | Senha deve ter complexidade (Maiúscula, Minúscula, Número, Especial). | CT-007 | Funcional, Regressivo, Automatizado | **Falhou** | Sim |
| **RN-CAD-07** | Confirmação de Senha deve ser idêntica à Senha. | CT-008 | Funcional, Regressivo, Automatizado | **Falhou** | Sim |
| **RN-CAD-08** | A senha não pode conter partes do nome ou e-mail. | CT-009 (Cadastro) | Funcional, Segurança | **Falhou** | Sim |

### 3.2 Login

| ID Requisito | Descrição do Requisito | Caso(s) de Teste | Tipo de Teste | Status | Defeito |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RF-LOG-01** | O usuário deve poder se logar. Login retorna Token (JWT/Session). | CT-009 (Login), CT-010 | Funcional, Smoke, Regressivo, Automatizado | **Passou** | — |
| **RN-LOG-01** | Mascaramento de Dados: API não deve retornar senha ou dados completos do cartão. | *Sem Cobertura* | — | **Risco de Qualidade** | — |
| **RN-LOG-02** | Sessão Stateless: Autenticação via Token (JWT). | *Sem Cobertura* | — | **Risco de Qualidade** | — |
| **RN-LOG-03** | Bloqueio de Força Bruta: Após 5 tentativas, bloquear por 15min ou CAPTCHA. | CT-013 | Funcional, Regressivo, Automatizado | **Falhou** | Sim |
| **RN-LOG-04** | Status Pendente: Conta UNVERIFIED. Login bloqueado até ativação. | CT-014 | Funcional, Regressivo | Não Executado | — |
| **RN-LOG-05** | Geração Código (OTP): Código numérico de 6 dígitos enviado por e-mail. | CT-015 | Funcional, Regressivo, Smoke | **Falhou** | Sim |
| **RN-LOG-06** | Expiração do Código: Validade de 15 minutos. | CT-016 | Funcional, Regressivo | **Falhou** | Sim |
| **RN-LOG-07** | Rate Limit Reenvio: Reenvio apenas a cada 60s. | CT-017 | Funcional, Regressivo | **Falhou** | Sim |
| **RN-LOG-08** | Tentativas Falhas (OTP): Após 3 erros, invalidar código atual. | CT-018 | Funcional, Regressivo | **Falhou** | Sim |

### 3.3 Catálogo

| ID Requisito | Descrição do Requisito | Caso(s) de Teste | Tipo de Teste | Status | Defeito |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RF-CTG-01** | Visualizar Catálogo: Grade com Imagem, Nome, Preço. | CT-019 | Funcional, Smoke, Regressivo, Automatizado | **Passou** | — |
| **RF-CTG-02** | Filtragem: Filtrar por Tags dinamicamente. | CT-020 | Funcional, Smoke, Regressivo, Automatizado | **Passou** | — |
| **RF-CTG-03** | Detalhes: Página com descrição, SKU, estoque. | CT-021 | Funcional, Smoke, Regressivo, Automatizado | **Passou** | — |
| **RN-CTG-01** | Visibilidade de Estoque: Botão desabilitado se sem estoque. | CT-022 | Funcional, Regressivo, Automatizado | **Passou** | — |
| **RN-CTG-02** | Integridade de Preço: Preço listagem == Preço detalhes. | CT-023 | Funcional, Regressivo, Automatizado | **Passou** | — |
| **RN-CTG-03** | Filtragem Tags (AND): Múltiplas tags funcionam como "E". | CT-024 | Funcional, Regressivo, Automatizado | **Passou** | — |

### 3.4 Carrinho

| ID Requisito | Descrição do Requisito | Caso(s) de Teste | Tipo de Teste | Status | Defeito |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RF-CAR-01** | Adicionar Item: Feedback visual imediato. | CT-025 | Funcional, Regressivo, Automatizado | **Passou** | — |
| **RF-CAR-02** | Manipular Carrinho: Alterar qtd, remover, recalcular subtotal. | CT-026, CT-027, CT-028 | Funcional, Regressivo, Automatizado | **Passou** (CT-026) | — |
| **RN-CAR-01** | Merge de Carrinhos: Transferir itens de anônimo para logado. | CT-029 | Funcional, Regressivo, Automatizado | Não Executado | — |
| **RN-CAR-02** | Validação Quantidade: Não permitir 0 ou negativo. | CT-030 | Funcional, Regressivo, Automatizado | Não Executado | — |
| **RN-CAR-03** | TTL: Carrinho anônimo expira em 24h. | CT-031 | Funcional, Regressivo | Não Executado | — |
| **RN-CAR-04** | Sincronização Preço: Validar preço em tempo real. | CT-032 | Funcional, Regressivo | Não Executado | — |

### 3.5 Pedido

| ID Requisito | Descrição do Requisito | Caso(s) de Teste | Tipo de Teste | Status | Defeito |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RF-PED-01** | Criação do Pedido: Consolida dados e limpa carrinho. | CT-033, CT-036 | Funcional, Regressivo, Automatizado | Não Executado | — |
| **RN-PED-01** | Endereço Obrigatório: Exige endereço válido. | CT-034 | Funcional, Regressivo, Automatizado | Não Executado | — |
| **RN-PED-02** | Imutabilidade: Snapshot do preço no momento da compra. | CT-035 | Funcional, Regressivo, Automatizado | Não Executado | — |
| **RN-PED-03** | Validação Final Estoque: Checagem de concorrência. | *Sem Cobertura* | — | **Risco de Qualidade** | — |

### 3.6 Pagamento

| ID Requisito | Descrição do Requisito | Caso(s) de Teste | Tipo de Teste | Status | Defeito |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RF-PAG-01** | Processamento: Validar e autorizar/negar transação. | CT-037, CT-038 | Funcional, Regressivo, Automatizado | Não Executado | — |
| **RN-PAG-01** | Validação Cartão: Rejeitar data vencida e Luhn inválido. | CT-039 | Funcional, Regressivo, Automatizado | Não Executado | — |
| **RN-PAG-02** | Antifraude: Transações > $100 marcadas como análise. | CT-041 | Funcional, Regressivo, Automatizado | Não Executado | — |
| **RN-PAG-03** | Idempotência: Evitar cobrança dupla. | CT-040 | Funcional, Regressivo, Automatizado | Não Executado | — |

---

## 4. Legenda

### Tipo
- **Funcional:** Regras de negócio e comportamento do sistema.
- **Não Funcional:** Performance, segurança, usabilidade, confiabilidade.

### Tipo de Teste
- Funcional
- Regressão
- E2E
- API
- Segurança
- Performance

### Status
- Não Executado
- Passou
- Falhou
- Bloqueado
- **Risco de Qualidade**: Requisito sem cobertura de teste identificada.

---

## 5. Regras de Atualização

- Todo requisito deve possuir pelo menos um caso de teste associado.
- Todo caso de teste deve rastrear ao menos um requisito.
- Requisitos sem cobertura devem ser sinalizados como **Risco de Qualidade**.
- Defeitos devem ser vinculados após abertura no Jira/GitHub Issues.

---

## 6. Benefícios da RTM

- Garantia de cobertura de testes.
- Visibilidade de impacto em mudanças.
- Apoio ao go/no-go da release.
- Evidência formal de qualidade.

---

## 7. Histórico de Versões

| Versão | Data | Descrição | Responsável |
| :--- | :--- | :--- | :--- |
| 1.0 | 25/01/2026 | Criação do documento | Matheus |