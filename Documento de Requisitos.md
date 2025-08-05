# Documento de Requisitos - Projeto VittaNext

## 1. Introdução

**Objetivo do Documento**
Este documento visa consolidar todos os requisitos funcionais, não funcionais, regras de negócio e módulos obrigatórios para o desenvolvimento da plataforma bancária digital VittaNext, conforme as diretrizes da disciplina de Análise e Projeto de Sistemas e o cenário realista fornecido pelo Banco VittaFácil .

**Objetivo do Sistema**
Criar uma plataforma bancária digital moderna, segura e responsiva, capaz de substituir o sistema legado, integrar-se a APIs públicas (BACEN, Serasa, Receita, PIX), e proporcionar autonomia ao cliente .

**Escopo e Limitações**

- **Escopo**: Módulos de Compra, Segurança, Comunicação e um módulo extra definido pela equipe.
- **Limitações**: Integração apenas com as APIs externas especificadas; protótipos funcionais sem implementação de back-end real.

## 2. Visão Geral do Sistema

**Atores Principais**

- **Cliente**
- **Atendente / Operador**

**Módulos**

1. **Compra**
2. **Segurança**
3. **Comunicação**
4. **Gestão Financeira Pessoal**

## 3. Regras de Negócio

1. Cliente só pode contratar empréstimo se não tiver restrição (SPC/Serasa)
2. Toda movimentação acima de R$ 5.000 deve ser registrada para compliance interno
3. Transações fora do perfil habitual exigem verificação adicional
4. Cliente pode cadastrar até 5 dispositivos confiáveis
5. Limite de saque diário de R$ 2.000, salvo exceções pré-aprovadas
6. Toda comunicação deve ser registrada e mantida por ≥ 5 anos
7. Cliente pode encerrar conta sem agência, não havendo pendências
8. Cartões virtuais: validade máxima 12 meses, exclusão a qualquer momento
9. A cada login malsucedido, gera-se alerta automático

## 4. Requisitos Funcionais

| Código | Descrição                                                                                 |
| ------ | ----------------------------------------------------------------------------------------- |
| RF01   | Permitir cadastro de usuários.                                                            |
| RF02   | Autenticação com senha criptografada e 2FA (OAuth 2.0, biometria, reconhecimento facial). |
| RF03   | Contratar empréstimo (consulta SPC/Serasa via Serasa API).                                |
| RF04   | Solicitar e ativar cartão (virtual e físico).                                             |
| RF05   | Aquisição de seguro.                                                                      |
| RF06   | Contratar pacotes de serviços bancários.                                                  |
| RF07   | Visualizar histórico de compras e cancelamentos.                                          |
| RF08   | Pagar via PIX (integração com API PIX do BACEN).                                          |
| RF09   | Enviar notificações (push, SMS, e-mail).                                                  |
| RF10   | Atender via chatbot com IA.                                                               |
| RF11   | Visualizar histórico de atendimentos e tickets.                                           |
| RF12   | Integração com WhatsApp Business.                                                         |
| RF13   | Fornecer sugestões automáticas com base no perfil de consumo.                             |
| RF14   | Enviar documentos e solicitações pelo app.                                                |
| RF15   | Visualizar relatório de gastos mensais.                                                   |
| RF16   | Definir orçamento mensal.                                                                 |
| RF17   | Receber sugestões personalizadas de economia.                                             |

## 5. Requisitos Não Funcionais

- **RNF01**: Disponibilidade 24×7.
- **RNF02**: Tempo de resposta de autenticação ≤ 3 s.
- **RNF03**: Interface responsiva (mobile-first).
- **RNF04**: Todas as comunicações criptografadas via HTTPS (TLS 1.3).
- **RNF05**: Criptografia de dados em trânsito e em repouso.
- **RNF06**: Logs armazenados e analisados (ELK Stack / Grafana).
- **RNF07**: Suporte a escalabilidade horizontal, tolerância a falhas e balanceamento de carga automático.
- **RNF08**: Conformidade com LGPD (rastreamento de acesso, anonimização de dados sensíveis).
- **RNF09**: Integração com APIs públicas: BACEN, Serasa, Receita Federal e PIX.

## 6. Módulos Obrigatórios

1. **Módulo de Compra**
   - RF03 a RF08
2. **Módulo de Segurança**
   - RF02 (2FA), + regras de criptografia e auditoria
3. **Módulo de Comunicação**
   - RF09 a RF14
4. **Módulo Adicional (Gestão Financeira Pessoal)**
   - RF15 a RF17
