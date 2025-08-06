# Documento de Requisitos – Projeto VittaNext (Atualizado)

## 1. Introdução

**Objetivo do Documento**
Consolidar todos os requisitos funcionais, não funcionais, regras de negócio e módulos obrigatórios para o desenvolvimento da plataforma bancária digital **VittaNext**, alinhando-os aos casos de uso definidos no arquivo de especificação **.puml**.

**Objetivo do Sistema**
Prover uma experiência bancária digital moderna, segura e responsiva, integrando-se a APIs públicas (BACEN, Serasa, Receita e PIX) e suportando operações de empréstimo, cartões, transações, comunicação e gestão financeira pessoal.

**Escopo e Limitações**

- **Escopo**: Funcionalidades de **Cadastro**, **Autenticação**, **Compra** (empréstimo, cartão, seguro, pacotes), **Transações PIX**, **Comunicação**, **Gestão Financeira**, **Dispositivos Confiáveis** e **Encerramento de Conta**.
- **Limitações**: Protótipo de front-end mobile-first; integrações simuladas ou via APIs públicas especificadas; sem backend legado.

## 2. Visão Geral do Sistema

**Atores**

- **Cliente**
- **Atendente / Operador**

**Módulos**

1. **Autenticação e Segurança**
2. **Compra**
3. **Comunicação**
4. **Gestão Financeira Pessoal**
5. **Gerenciamento de Conta**
6. **Transferências**

## 3. Regras de Negócio

1. Cliente só pode contratar empréstimo se não tiver restrição no **SPC/Serasa** e cadastro regular no **BACEN**.
2. Cliente pode registrar até **5 dispositivos confiáveis** para 2FA.
3. Limite de saque diário de **R$ 2.000**, ajustável via aprovação.
4. Movimentações acima de **R$ 5.000** geram alerta para compliance.
5. Transações fora do perfil exigem verificação adicional.
6. Cartões virtuais têm validade máxima de **12 meses**.
7. Fluxos de login malsucedido geram **notificação de segurança**.
8. Todas as comunicações e transações são mantidas por **≥ 5 anos** (logs).
9. Encerramento de conta só após quitação de pendências (saldo e contratos).

## 4. Requisitos Funcionais

| Código   | Título                   | Descrição Detalhada                                          |
| -------- | ------------------------ | ------------------------------------------------------------ |
| **RF01** | Cadastro de Usuário      | Cadastro de dados pessoais (nome, CPF, e-mail) gerando perfil na plataforma. |
| **RF02** | Autenticação             | Login com senha criptografada e 2FA por SMS ou app confiável. |
| **RF03** | Dispositivo Confiável    | Registro de dispositivo móvel para autenticação sem código em acessos futuros. |
| **RF04** | Encerramento de Conta    | Encerrar conta com verificação de pendências e confirmação final do cliente. |
| **RF05** | Empréstimo               | Solicitação de empréstimo com consulta a Serasa e BACEN, cálculo de proposta. |
| **RF06** | Solicitação de Cartão    | Pedido de cartão virtual ou físico, com confirmação de dados e envio. |
| **RF07** | Ativação de Cartão       | Ativação do cartão atualizado status para uso após validação. |
| **RF08** | Contratação de Seguro    | Escolha de apólice de seguro bancário e confirmação de condições contratuais. |
| **RF09** | Pacotes de Serviços      | Seleção e contratação de planos de tarifas e serviços bancários. |
| **RF10** | Histórico de Compras     | Exibição de todas as transações de compra e cancelamentos pelos clientes. |
| **RF11** | Pagamento via PIX        | Pagamento instantâneo via PIX com integração à API do BACEN. |
| **RF12** | Notificações             | Envio de alertas e atualizações por push, SMS ou e-mail conforme preferência. |
| **RF13** | Chatbot e WhatsApp       | Atendimento automatizado via chatbot e canal WhatsApp Business. |
| **RF14** | Histórico de Atendimento | Registro e consulta de tickets de suporte gerados pelo usuário. |
| **RF15** | Envio de Documentos      | Upload e envio de documentos para solicitações e validações. |
| **RF16** | Relatório de Gastos      | Geração de relatório mensal de despesas, agrupadas por categoria. |
| **RF17** | Orçamento Mensal         | Definição de limites de gastos por categoria para controle financeiro. |
| **RF18** | Sugestões de Economia    | Sugestões personalizadas de economia baseadas no perfil de consumo. |
| **RF19** | Pagar boleto             | O usuário deve ser capaz de realizar pagamentos de boletos pelo aplicativo. |
| **RF20** | Transferir via TED       | Deve ser possível transferir via TED com integração à API do BACEN. |

## 5. Requisitos Não Funcionais

| Código    | Descrição                                                    |
| --------- | ------------------------------------------------------------ |
| **RNF01** | Disponibilidade 24×7 para acesso contínuo ao app.            |
| **RNF02** | Tempo de resposta ≤ 3 segundos em operações críticas como login e transações. |
| **RNF03** | Interface mobile-first responsiva para iOS e Android.        |
| **RNF04** | Criptografia TLS 1.3 em todas as comunicações de rede.       |
| **RNF05** | Criptografia avançada de dados em repouso e em trânsito.     |
| **RNF06** | Logs centralizados e analisáveis via ELK Stack e Grafana para monitoramento e auditoria. |
| **RNF07** | Suporte a escalabilidade horizontal e alta disponibilidade com orquestração de containers. |
| **RNF08** | Conformidade com LGPD garantindo anonimização e rastreabilidade de dados pessoais. |
| **RNF09** | Integração com APIs externas (BACEN, Serasa, Receita Federal, PIX e SMS Gateway). |
