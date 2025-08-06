# **UC-01**

| Nome do Caso de Uso | Abrir Conta UC-01 |
| ----- | :---- |
| **Caso de Uso Geral** | UC-01 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Permite que novos usuários criem uma conta digital informando dados e documentos |
| **Pré-condições** | Usuário não possuir conta prévia no banco |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Abrir Conta”. |  |
| 2\. Informar dados pessoais (nome, CPF, e‑mail, telefone, endereço). |  |
| 3\. Enviar documentos escaneados (RG/CPF, comprovante de residência). |  |
|  | 4\. Validar dados básicos e documentos. |
|  | 5\. O sistema gera conta provisória e envia e‑mail/SMS de boas‑vindas. |
| **Restrições/Validações** |  |
| **Fluxo Alternativo 3A – Documento inválido ou ilegível** |  |
| **Ações do Ator** | **Ações do Sistema** |
|  | 1\. Sistema rejeita e solicita reenvio. |

# 

# **UC-02**

| Nome do Caso de Uso | Encerrar Conta |
| ----- | :---- |
| **Caso de Uso Geral** | UC-02 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para encerrar uma conta |
| **Pré-condições** | Cliente não ter pendências financeiras ou contratuais. |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Encerrar Conta”. |  |
|  | 2\. Sistema verifica pendências (saldo, empréstimos, tarifas) |
|  | 3\. Sistema exibe termo de encerramento |
| 4\. Cliente confirma os termos de encerramento |  |
|  | 5\. Sistema baixa a conta e revoga acessos |
|  | 6\. Envia protocolo e confirmação por e‑mail |
| **Restrições/Validações** |  |
|  |  |
| **Fluxo Alternativo 2A \- Pendências encontradas** |  |
| **Ações do Ator** | **Ações do Sistema** |
|  | 1\. Sistema lista pendências e orienta regularização antes do encerramento |

# **UC-03**

| Nome do Caso de Uso | Adicionar Dispositivo Confiável |
| ----- | :---- |
| **Caso de Uso Geral** | UC-03 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para adicionar um novo dispositivo à lista de dispositivos confiáveis do cliente |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Dispositivos Confiáveis” em “Segurança” |  |
| 2\. Cliente seleciona “Adicionar novo dispositivo” |  |
|  | 3\. Sistema envia código de verificação para e‑mail/SMS |
| 4\. Cliente insere código e confirma |  |
|  | 5\. Dispositivo é marcado como confiável |
| **Restrições/Validações** |  |
| 1\. Cliente possuir, no máximo 5 dispositivos classificados como confiáveis |  |
| **Fluxo de Exceção 3A \- 5 dispositivos confiáveis** |  |
|  | 1\. Sistema bloqueia inclusão e sugere remoção de um existente |

# **UC-04**

| Nome do Caso de Uso | Login |
| ----- | :---- |
| **Caso de Uso Geral** | UC-04 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para realizar login  |
| **Pré-condições** | O cliente estar cadastrado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente informa CPF e senha |  |
|  | 2\. Sistema valida credenciais |
|  | 3\. Se configurado, envia OTP ou solicita biometria |
|  | 4\. Acesso liberado e direcionado a tela principal |
| **Restrições/Validações** |  |
| 1\. A cada tentativa de login malsucedida, gerar alerta imediato |  |
| **Fluxo Alternativo 2A \- Senha incorreta** |  |
| **Ações do Ator** | **Ações do Sistema** |
|  | 1\. Solicita a senha novamente  |
| 2\. Digita a senha |  |
|  | 3\. Na  6ª tentativa a conta é bloqueada |

# **UC-05**

| Nome do Caso de Uso | Autenticação 2FA  |
| ----- | :---- |
| **Caso de Uso Geral** | UC-05 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para ativar autenticação de dois fatores |
| **Pré-condições** | Cliente estar autenticado e dispositivo marcado como confiável |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
|  | 1\. Sistema envia OTP por app autenticador, SMS ou e‑mail |
| 2\. Cliente insere código ou faz leitura biométrica  |  |
|  | 3\. Sistema valida segundo fator |
| **Fluxo Alternativo 2A – Erro na leitura biométrica ou código inválido** |  |
| **Ações do Ator** | **Ações do Sistema** |
|  | 1\. Solicita nova leitura biométrica ou gera novo código |
| 2\. Insere a biometria ou código |  |

# **UC-06**

| Nome do Caso de Uso | Visualizar Saldo |
| ----- | :---- |
| **Caso de Uso Geral** | UC-06 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente visualizar o saldo |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Visualizar Saldo” |  |
|  | 2\. Sistema consulta saldo disponível junto ao core bancário |
|  | 3\. Exibe saldo em tela |

# **UC-07**

| Nome do Caso de Uso | Saque/Depósito |
| ----- | :---- |
| **Caso de Uso Geral** | UC-07 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente realizar saque/depósito |
| **Pré-condições** | 1\. Cliente estar autenticado |
|  | 2\. Para saque, dispositivo marcado como confiável ou 2FA completo |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente escolhe “Saque/Depósito |  |
| 2\. Informar  tipo de operação e valor |  |
|  | 3\. Para saque, sistema verifica limite diário (R$ 2.000) – exceções somente se pré‑aprovadas |
|  | 4\. Solicita confirmação por 2FA ou token |
|  | 5\. Opera transação junto ao canal físico (ATM/Caixa) ou core |
|  | 6\. Exibe comprovante e atualiza histórico |
| **Restrições/Validações** |  |
| 1\. Limite de saque diário: R$ 2.000 (salvo exceções aprovadas) |  |
| 2\. Movimentações \> R$ 5.000 geram registro de compliance |  |
| 3\. Transações atípicas exigem verificação adicional |  |
| **Fluxo Alternativo 3A \-  Valor acima do limite** |  |
| **Ações do Ator** | **Ações do Sistema** |
|  | 1\. Sistema bloqueia e sugere solicitação de exceção pré‑aprovada |

# **UC-08**

| Nome do Caso de Uso | Realizar Transferência via PIX |
| ----- | :---- |
| **Caso de Uso Geral** | UC-08 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente realizar transferências via PIX |
| **Pré-condições** | 1\. Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “PIX” \> “Fazer PIX” |  |
| 2\. Informa chave, valor e descrição |  |
|  | 3\. Sistema valida limites e perfil de segurança |
|  | 4\. Solicita confirmação via token/biometria |
|  | 5\. Executa transferência junto ao PSP do PIX |
|  | 6\. Exibe comprovante e notifica cliente |
| **Restrições/Validações** |  |
| 1\. Movimentações \> R$ 5.000 geram registro de compliance |  |
| 2\. Transações atípicas exigem verificação adicional |  |
| **Fluxo de Exceção 3A \- Valor acima do limite diário** |  |
|  | 1\. Bloqueio automático |
| **Fluxo de Exceção 4A \- Falha na autenticação** |  |
|  | 1\. Cancela operação |

**UC-09**

| Nome do Caso de Uso | Realizar Transferência via TED |
| ----- | :---- |
| **Caso de Uso Geral** | UC-09 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente realizar transferências via TED |
| **Pré-condições** | 1\. Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “TED” \> “Fazer transferência” |  |
| 2\. Informa conta, valor e descrição |  |
|  | 3\. Sistema valida limites e perfil de segurança |
|  | 4\. Solicita confirmação via token/biometria |
|  | 5\. Executa transferência junto ao BACEN |
|  | 6\. Exibe comprovante e notifica cliente |
| **Restrições/Validações** |  |
| 1\. Movimentações \> R$ 5.000 geram registro de compliance |  |
| 2\. Transações atípicas exigem verificação adicional |  |
| **Fluxo de Exceção 4A \- Falha na autenticação** |  |
|  | 1\. Cancela operação |

# **UC-10**

| Nome do Caso de Uso | Pagar Contas |
| ----- | :---- |
| **Caso de Uso Geral** | UC-10 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente pagar contas |
| **Pré-condições** | 1\. Cliente estar autenticado |
|  | 2\. Cliente ter saldo suficiente |
| **Pós-condições** | Boleto ou código de barras estar disponível |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente escolhe “Pagar Contas” |  |
|  | 2\. Ler ou digitar código de barras |
|  | 3\. Sistema busca dados (destinatário, valor e vencimento) |
| 4\. Cliente confirma e faz autenticação via 2FA |  |
|  | 5\. Sistema realiza débito e envia o comprovante |
| **Restrições/Validações** |  |
| 1\. Verificar saldo do cliente |  |
| 2\. Movimentações \> R$ 5.000 geram registro de compliance |  |
| 3\. Transações atípicas exigem verificação adicional |  |

# **UC-11**

| Nome do Caso de Uso | Solicitar Empréstimo |
| ----- | :---- |
| **Caso de Uso Geral** | UC-11 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente solicitar empréstimo |
| **Pré-condições** | 1\. Cliente estar autenticado |
|  | 2\. O cliente não ter pendências |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Empréstimos” \> “Solicitar Empréstimo” |  |
| 2\. Informa valor |  |
|  | 3\. Sistema consulta crédito e histórico de movimentações |
|  | 4\. Se aprovado, apresenta taxas, parcelas e CET |
| 5\. Cliente confirma e assina digitalmente |  |
|  | 6\. Creditar valor em conta |
| **Restrições/Validações** |  |
| 1\. Cliente só pode contratar empréstimo se estiver sem restrições no SPC/Serasa |  |
| 2\. Movimentações \> R$ 5.000 geram registro de compliance |  |
| 3\. Transações atípicas exigem verificação adicional |  |
| **Fluxo de Exceção 3A \- Restrição cadastral** |  |
| **Ações do Ator** | **Ações do Sistema** |
|  | 1\. Nega solicitação e orienta regularização |

# **UC-12**

| Nome do Caso de Uso | Solicitar Cartão |
| ----- | :---- |
| **Caso de Uso Geral** | UC-12 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente solicitar cartão |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** | Cartão criado no módulo de Compras |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente escolhe “Solicitar Cartão” |  |
| 2\. Seleciona tipo (físico ou virtual) |  |
|  | 3\. Sistema verifica elegibilidade |
|  | 4\. Em caso de cartão virtual: emite número válido por até 12 meses |
|  | 5\. Envia via correio ou disponibiliza no app |
| **Restrições/Validações** |  |
| 1\. Cartões virtuais válidos por 12 meses, excluíveis a qualquer instante |  |

# **UC-13**

| Nome do Caso de Uso | Adquirir Seguro |
| ----- | :---- |
| **Caso de Uso Geral** | UC-13 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente adquirir seguro |
| **Pré-condições** | Cliente estar autenticado   |
| **Pós-condições** | Apólice armazenada no módulo de Compras |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Seguros” \> “Adquirir Seguro” |  |
| 2\. Escolhe produto e cobre frações (ex.: vida, proteção de cartão) |  |
|  | 3\. Sistema calcula prêmio e condições |
| 4\. Cliente confirma e assina digitalmente |  |
|  | 5\. Apólice gerada e enviada por e‑mail |
| **Restrições/Validações** |  |
| 1\. Movimentações \> R$ 5.000 geram registro de compliance |  |
| 2\. Transações atípicas exigem verificação adicional |  |
| 3\. O cliente precisa fornecer algum comprovante de residência |  |

# **UC-14**

| Nome do Caso de Uso | Contratar Pacote de Serviços |
| ----- | :---- |
| **Caso de Uso Geral** | UC-14 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente contratar serviços |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** | Serviço ativo e histórico de cobranças iniciado |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Pacotes de Serviços” |  |
| 2\. Seleciona pacote (ex.: cashback, investimentos) |  |
|  | 3\. Disponibiliza condições e periodicidade |
| 4\. Confirma contratação |  |
|  | 5\. Sistema inicia cobrança periódica |

# **UC-15**

| Nome do Caso de Uso | Consultar Histórico de Compras |
| ----- | :---- |
| **Caso de Uso Geral** | UC-15 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente consultar histórico de compras |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Histórico de Compras” |  |
|  | 2\. Sistema lista todas as operações de compra (cartões, seguros, pacotes) |
| 3\. Cliente filtra por período ou tipo |  |

# **UC-16**

| Nome do Caso de Uso | Consultar Histórico de Cancelamentos |
| ----- | :---- |
| **Caso de Uso Geral** | UC-16 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente consultar histórico de cancelamentos |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Histórico de Cancelamentos”. |  |
|  | 2\. Sistema exibe serviços ou produtos cancelados com data e motivo |

# **UC-17**

| Nome do Caso de Uso | Enviar Documentos |
| ----- | :---- |
| **Caso de Uso Geral** | UC-17 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente enviar documentos |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente escolhe “Enviar Documentos” no módulo de Comunicação |  |
| 2\. Cliente anexa arquivos (PDF, imagens) |  |
|  | 3\. Sistema valida tipo/tamanho e armazena |
|  | 4\. Confirmação de recebimento é exibida |

# **UC-18**

| Nome do Caso de Uso | Aderir ao Canal de WhatsApp |
| ----- | :---- |
| **Caso de Uso Geral** | UC-18 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente entrar no canal de WhatsApp do banco |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente clica em “Aderir ao Canal de WhatsApp” |  |
|  | 2\. Sistema envia link de confirmação |
| 3\. Cliente confirma no WhatsApp |  |
|  | 4\. Canal é ativado para notificações futuras |

# **UC-19**

| Nome do Caso de Uso | Receber Notificações |
| ----- | :---- |
| **Caso de Uso Geral** | UC-19 |
| **Ator Principal** | Cliente |
| **Atores Secundários** | notificação  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente receber notificações |
| **Pré-condições** | 1\. Cliente estar autenticado |
|  | 2\. Ter pelo menos um canal de notificação configurado (SMS, Push ou E‑mail) |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Sistema envia notificações de eventos (transações, faturas, avisos) |  |
|  | 2\. Cliente recebe notificações no canal configurado |
| **Restrições/Validações** |  |
| 1\. Toda comunicação deve ser registrada e mantida por 5 anos |  |

# **UC-20**

| Nome do Caso de Uso | Interagir com Chatbot |
| ----- | :---- |
| **Caso de Uso Geral** | UC-20 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente interagir com chatbot |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Cliente acessa “Chatbot” no módulo de Comunicação |  |
| 2\. Digita ou escolhe opções de atendimento |  |
|  | 3\. Chatbot responde com base em FAQ ou direciona para atendente |
| **Restrições/Validações** |  |
| 1\. Toda comunicação deve ser registrada e mantida por 5 anos |  |

# **UC-21**

| Nome do Caso de Uso | Visualizar Histórico de Suporte |
| ----- | :---- |
| **Caso de Uso Geral** | UC-21 |
| **Ator Principal** | Cliente ou Atendente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente Visualizar histórico de suporte |
| **Pré-condições** | Cliente estar autenticado ou atendente com permissão |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Usuário acessa “Histórico de Suporte” |  |
|  | 2\. Sistema exibe todas as interações (chatbot, atendente) |
| 3\. Cliente/atendente pode filtrar por data ou tipo |  |
| **Restrições/Validações** |  |
| 1\. Registrar toda comunicação e manter por 5 anos |  |

# **UC-22**

| Nome do Caso de Uso | Relatório de gastos |
| ----- | :---- |
| **Caso de Uso Geral** | UC-22 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente visualizar o Relatório de gastos |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Usuário acessa “Relatório de Gastos” |  |
|  | 2\. Sistema exibe todos os gastos |
| 3\. Cliente pode filtrar por categoria e/ou tempo |  |

# **UC-23**

| Nome do Caso de Uso | Orçamento Mensal |
| ----- | :---- |
| **Caso de Uso Geral** | UC-23 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente visualizar o Orçamento Mensal |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Usuário acessa “Orçamento Mensal” |  |
| 2\. Cliente define valores por categoria |  |
|  | 3\. Sistema salva alterações |

# **UC-24**

| Nome do Caso de Uso | Sugestões financeiras |
| ----- | :---- |
| **Caso de Uso Geral** | UC-24 |
| **Ator Principal** | Cliente |
| **Atores Secundários** |  |
| **Resumo** | Esse caso de uso descreve as etapas percorridas para o cliente visualizar sugestões financeiras do sistema |
| **Pré-condições** | Cliente estar autenticado |
| **Pós-condições** |  |
| **Fluxo Principal** |  |
| **Ações do Ator** | **Ações do Sistema** |
| 1\. Usuário acessa “Sugestões” |  |
|  | 2\. Sistema recupera histórico de gastos e analisa perfil de consumo |
|  | 3\. Gera sugestões com base em IA/regras e as exibe |

