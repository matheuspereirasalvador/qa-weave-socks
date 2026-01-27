# Plano de Testes - ISO 29119-3 

## 1. Objetivo

Validar as funcionalidades do sistema, a partir do Home até o pedido confirmado (MVP)

## 2. Versão
| Versão | Data | Autor | Descrição/Alterações |
| :--- | :--- | :--- | :--- |
| 1.0 | 20/01/2026 | Matheus | Criação do documento |

## 3. Escopo
Defina o que será testado
* **No Escopo:** (Catálogo, Carrinho, Identidade, Pedido e Pagamento)


## 4. Equipe
Liste os membros envolvidos e suas responsabilidades.
| Nome | Papel | Responsabilidade |
| :--- | :--- | :--- |
| Matheus | QA Lead | Definir estratégia e revisar casos |

## 5. Riscos
* **Risco:** Lotação de banco de dados
* **Mitigação:** Resetar o banco de dados a cada teste.
---
* **Risco:** Ficar sem dados para testes
* **Mitigação:** Gerar uma grande massa de dados antes dos testes
---
* **Risco:** Falta de experiência com ferramentas
* **Mitigação:** Estudar durante algumas horas as ferramentas
---

## 6. Estratégia de Testes
Descreva a abordagem geral para os testes.
* **Tipos de Teste:** (Funcionais, Regressivos, Perfomance, Segurança, Usabilidade, Portabilidade e Exploratório).
* **Níveis de Teste:** (Integração, Sistema, Aceite).
* **Ferramentas:** Jira(Zephyr), Cypress(Automação), Postman(API), Dbeaver(SQL), k6(Performance), OWASP (Segurança).
* **Dados de Teste:** Faker.

## 7. Atividades e Estimativas
| Atividade | Responsável | Estimativa (Horas/Dias) | Data Início | Data Fim |
| :--- | :--- | :--- | :--- | :--- |
| Planejamento | QA Lead | 3h | 19/01 | 20/01 |
| Escrita de Casos | QA Lead| 4h | 20/01 | 24/01 |
| Execução | QA Lead | 8h | 24/01 | 01/02 |