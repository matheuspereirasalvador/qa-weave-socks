# Matriz de Rastreabilidade de Testes (RTM)
**Padrão:** ISO/IEC/IEEE 29119-3 & ISTQB
**Projeto:** _______________________
**Versão do Documento:** 1.0
**Data:** __/__/____
**Autor/Gerente de Teste:** _______________________

---

## 1. Legenda e Status

* **Prioridade (Risco):** (A)lta, (M)édia, (B)aixa.
* **Status de Execução:**
    * ⚪ **Não Iniciado:** Planejado, mas não executado.
    * ✅ **Passou:** Resultado esperado atingido.
    * ❌ **Falhou:** Resultado diverge do esperado (Bug).
    * ⚠️ **Bloqueado:** Impossível executar (dependência/ambiente).
    * 🚫 **Descartado:** Fora do escopo atual.

---

## 2. Matriz de Rastreabilidade

| ID Base de Teste (Req/User Story) | Descrição do Requisito | Prioridade (Risco) | ID Condição de Teste | ID Caso de Teste | Descrição do Caso de Teste | Referência (Script/Arquivo) | Status Execução | ID Defeito (Bug) |
| :--- | :--- | :---: | :--- | :--- | :--- | :--- | :---: | :---: |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |
| | | | | | | | ⚪ | |

---

## 3. Resumo de Cobertura (Métricas de Controle)

| Métrica | Valor Atual | Meta / SLA |
| :--- | :---: | :---: |
| **Total de Requisitos/Histórias** | 0 | - |
| **Cobertura de Requisitos (%)** | 0% | 100% |
| **Total de Casos de Teste** | 0 | - |
| **% Execução Planejada** | 0% | 100% |
| **Taxa de Pass (Sucesso)** | 0% | > 95% |
| **Total de Defeitos Abertos** | 0 | 0 |

---

### Notas de Preenchimento (Guia Rápido ISO 29119)

1.  **ID Base de Teste:** O identificador único do requisito (ex: `REQ-001`, `US-102`) vindo da documentação funcional.
2.  **ID Condição de Teste:** O item específico sendo verificado dentro daquele requisito (ex: `COND-001` - Validação de Senha Forte). Um requisito pode ter várias condições.
3.  **ID Caso de Teste:** O identificador do roteiro de teste (ex: `CT-auth-001`).
4.  **Referência:** Link para o script de automação (Github/Gitlab) ou ferramenta de gestão (Jira/Azure DevOps).
5.  **ID Defeito:** Obrigatório preencher caso o status seja ❌ **Falhou**. Isso garante a rastreabilidade do problema.