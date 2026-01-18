# Especificação de Requisitos de Software (SRS)

**Projeto:** WeaveSocks
**Versão:** 1.0
**Data:** 18/01/2026
**Status:** Em andamento
**Autores:** Matheus

---

## 1. Introdução

Este documento descreve os requisitos funcionais e não-funcionais do sistema WeaveSocks, com o objetivo de garantir clareza, rastreabilidade e alinhamento entre as áreas de Produto, Desenvolvimento e Qualidade.

### 1.1 Objetivo

Definir de forma clara o comportamento esperado do sistema, suas regras de negócio, integrações e restrições técnicas, servindo como base para:

- Planejamento de testes
- Criação da matriz de rastreabilidade
- Execução de testes funcionais e não funcionais
- Automação
- Validação de aceite

### 1.2 Escopo

Este documento cobre os módulos:

- Catálogo
- Carrinho
- Identidade
- Pedido
- Pagamento

Itens fora deste escopo não serão considerados nesta versão.

---

## 2. Visão Geral do Sistema

O Sock Shop é um e-commerce especializado na venda de meias de alta qualidade. O sistema deve permitir que usuários (visitantes e registrados) naveguem pelo catálogo, filtrem produtos, gerenciem um carrinho de compras e finalizem pedidos. A arquitetura é baseada em microsserviços, o que exige atenção redobrada em testes de integração e contrato.

### 2.2 Arquitetura (se aplicável)

- Tipo: Microsserviços
- Comunicação: REST 
- Bancos de dados: SQL (MySQL) | NoSQL (MongoDB)
- Autenticação: JWT (ID LOGIN) | Session (Cookie) |

---

# 🔹 PADRÃO DE MÓDULOS

## 3. Módulo

### Catalogo
> **Stack:** GO e MySQL

### Carrinho
> **Stack:** Java e MongoDB

### Identidade
> **Stack:** GO e MongoDB

### Pedido
> **Stack:** Java/.NET e MongoDB

### Pagamento
> **Stack:** GO

---

### 3.1 Requisitos Funcionais (RF)

#### 3.1.1 Catálogo

| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RF-CTG-01** | Visualizar Catálogo | O usuário deve visualizar uma grade de produtos na Home Page e cada card deve exibir: Imagem, Nome, Preço e botão "Adicionar ao Carrinho". |
| **RF-CTG-02** | Filtragem de Produtos | O usuário deve poder filtrar produtos por Tags (ex: sport, formal, blue, red) e a filtragem deve ser dinâmica (sem recarregar a página inteira, via AJAX/API) |
| **RF-CTG-03** | Detalhes do Produto | Ao clicar em um produto, o usuário deve ver a página de detalhes contendo: Descrição completa, SKU, Estoque restante e Opções de especificação (se houver). |

---

#### 3.1.2 Carrinho

| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RF-CAR-01** | Adicionar Item | O usuário pode adicionar itens ao carrinho a partir da Home ou da Página de Detalhes e feedback visual imediato deve ser exibido ("Item adicionado"). |
| **RF-CAR-02** | Manipular Carrinho| O usuário pode alterar a quantidade de itens, o usuário pode remover itens (Delete) e subtotal deve ser recalculado em tempo real. |

---

#### 3.1.3 Identidade

| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RF-IDEN-01** | Login e Registro | O usuário deve poder se cadastrar fornecendo: Nome, Sobrenome, Email e Senha. O login também deve retornar um Token (JWT ou Session ID) que autentica as chamadas subsequentes para os microsserviços de Pedido e Pagamento. |

---

#### 3.1.4 Pedido

| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RF-PED-01** | Criação do Pedido | Deve ser acionado somente após o retorno positivo do Pagamento, o pedido deve consolidar: Itens do Carrinho + Endereço de Entrega + ID do Pagamento Autorizado, o pedido  também deve ser salvo no banco Mongo do serviço de Orders. Após criar o pedido, o serviço deve limpar o carrinho do usuário. |

---

#### 3.1.4 Pagamento
| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RF-PAG-01** | Processamento de Pagamento | O serviço deve receber o ID do cliente, o valor total e os dados do cartão (número, CCV e validade), sem acessar detalhes dos itens. O comportamento consiste em validar o formato do cartão via algoritmo de Luhn para verificar sua integridade. A saída do sistema deve ser estritamente "Autorizado" para cartões válidos ou "Negado" para inconsistências.|


---

### 3.2 Regras de Negócio (RN)

#### 3.2.1 Catálogo
| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RN-CTG-01** | Visibilidade de Estoque | O catálogo pode exibir produtos sem estoque, mas o botão "Adicionar ao Carrinho" deve estar desabilitado ou o produto deve conter uma tag visual "Sold Out".|
| **RN-CTG-02** |Integridade de Preço | O preço exibido na listagem (Home) deve ser idêntico ao preço na página de detalhes. Divergências visuais são consideradas defeito crítico. |
| **RN-CTG-03** | Filtragem de Tags | Ao selecionar múltiplas tags, o filtro deve funcionar como uma operação "OU" (ex: "blue" + "sport" exibe meias que sejam blue OU sport) |

---

#### 3.2.2 Carrinho
| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RN-CAR-01** | Merge de Carrinhos | Se um usuário anônimo adicionar itens ao carrinho e depois fizer login, esses itens devem ser transferidos para o carrinho persistido do usuário logado. Exceção: Se o item já existir no carrinho do usuário, a quantidade deve ser somada.|
| **RN-CAR-02** | Validação de Quantidade | Não é permitido adicionar 0 (zero) ou quantidades negativas de itens. O input deve ser sanitizado. |
| **RN-CAR-03** | TTL (Time-to-Live) | Carrinhos de usuários anônimos expiram após 24 horas de inatividade para limpeza de banco (Redis/Mongo). Carrinhos de usuários logados não expiram. |
| **RN-CAR-04** | Sincronização de Preço| O preço dos itens no carrinho deve ser sempre consultado em tempo real no serviço de Catálogo. Se houver divergência entre o preço no momento da adição e o preço atual (ex: fim de promoção), o sistema deve considerar o preço atual do Catálogo no momento do Checkout. Opcional (Nice to have): Exibir um alerta para o usuário: "O preço de alguns itens no seu carrinho mudou". |

---

#### 3.2.3 Identidade
| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RN-IDEN-01** | Unicidade de Cadastro| Não é permitido cadastrar dois usuários com o mesmo e-mail. O sistema deve retornar mensagem amigável ("E-mail já cadastrado").|
| **RN-IDEN-02** | Mascaramento de Dados | A API de retorno de dados do usuário (GET /customers/{id}) nunca deve retornar a senha (nem hash) ou os dados completos do cartão de crédito salvo (apenas os últimos 4 dígitos). |
| **RN-IDEN-03** | Sessão Stateless | A autenticação deve ocorrer via Token (JWT). O sistema não deve depender de session sticky no servidor, permitindo que qualquer instância do serviço de usuário valide a requisição. |

---

#### 3.2.4 Pedido
| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RN-PED-01** | Endereço Obrigatório | Um pedido não pode ser criado sem um vínculo com um endereço de envio (Shipping Address) válido e completo. |
| **RN-PED-02** | Imutabilidade Histórica | Uma vez criado, os itens e preços de um pedido não podem ser alterados, mesmo que o preço do produto mude posteriormente no Catálogo. O pedido deve gravar um "snapshot" do preço no momento da compra. |
| **RN-PED-03** | Validação Final de Estoque | No momento exato da criação do pedido (após pagamento), o serviço deve fazer a última checagem de estoque. Se falhar aqui, o pedido é cancelado e o pagamento estornado (cenário de concorrência). |

---

#### 3.2.5 Pagamento
| ID | Título | Descrição |
| :--- | :--- | :--- |
| **RN-PAG-01** | Validação de Cartão | O sistema deve validar o formato do número do cartão (algoritmo de Luhn) antes de tentar processar. Datas de validade anteriores ao mês atual devem ser rejeitadas imediatamente. |
| **RN-PAG-02** | Regra Antifraude (Simulada) | Transações com valor total superior a $100.00 devem ser marcadas como "Analise de Risco" nos logs, mas aprovadas se o cartão for válido (para fins deste MVP). |
| **RN-PAG-03** | Idempotência | Se o usuário clicar duas vezes em "Pagar", o sistema deve identificar a duplicidade (via ID da transação ou token de idempotência) e não cobrar duas vezes. |

---

## 4. Requisitos Não-Funcionais (RNF)

| ID | Categoria | Descrição |
| :--- | :--- | :--- |
| **RNF-01** | Performance | O tempo de carregamento da Home Page e listagem do Catálogo não deve exceder **2 segundos** para 95% das requisições (p95 latency) sob carga normal. O processamento síncrono do Checkout (Pagamento + Criação de Pedido) deve ocorrer em no máximo **3 segundos**. |
| **RNF-02** | Segurança | Toda a comunicação entre o cliente e os serviços deve ser criptografada via **TLS/HTTPS**. As senhas dos usuários devem ser armazenadas utilizando algoritmos de hash robustos (ex: BCrypt) com *salt*. A autenticação deve utilizar tokens **JWT (JSON Web Tokens)**. |
| **RNF-03** | Usabilidade | A interface deve ser **Responsiva**, garantindo usabilidade total em dispositivos móveis (breakpoints padrão). Mensagens de erro de sistema (ex: 500) devem ser tratadas e exibidas de forma amigável, sem expor stack traces. |
| **RNF-04** | Confiabilidade | O sistema deve implementar o padrão **Circuit Breaker**. Se um serviço não crítico falhar, a página deve degradar graciosamente (Graceful Degradation). Garantia de disponibilidade de **99.9%** em horário comercial. |
| **RNF-05** | Escalabilidade | Microsserviços críticos (`Front-end`, `Catalogue`, `Order`) devem suportar **Escalabilidade Horizontal Automática (HPA)** quando o uso de CPU ultrapassar **70%**. Suporte a picos de até **1.000 usuários simultâneos**. |

---



## 5. Critérios de Aceite

- Todos os requisitos funcionais implementados
- Nenhum bug crítico ou blocker
- Testes executados e documentados
- Evidências registradas

---

## 6. Rastreabilidade

Todos os requisitos descritos neste documento deverão ser vinculados a:

- Histórias no Jira
- Casos de teste
- Execuções
- Bugs

(Ver Matriz de Rastreabilidade) 

---

## 7. Histórico de Versões

| Versão | Data | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 1.0 | 18/01/2026 | Criação do documento | Matheus |

