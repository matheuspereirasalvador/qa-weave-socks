# Matriz de Rastreabilidade de Requisitos (RTM)

**Projeto:** <Nome do Projeto>  
**Versão:** 1.0  
**Data:** <DD/MM/AAAA>  
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
- Casos de Teste
- Tipo de Teste
- Status de Execução
- Defeitos associados

---

## 3. Matriz de Rastreabilidade

| ID Requisito | Tipo | Descrição do Requisito | Módulo | Caso(s) de Teste | Tipo de Teste | Status | Defeito |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| RF-001 | Funcional | <Descrição do requisito> | <Módulo> | CT-001 | Funcional | Não Executado | — |
| RF-002 | Funcional | <Descrição do requisito> | <Módulo> | CT-002, CT-003 | E2E | Não Executado | — |
| RNF-001 | Não Funcional | <Descrição RNF> | Sistema | Performance | Performance | Não Executado | — |

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
| 1.0 | <DD/MM/AAAA> | Criação do documento | Matheus |
