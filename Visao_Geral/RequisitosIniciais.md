# FORMULÁRIO - LEVANTAMENTO INICIAL DE REQUISITOS
 
**Projeto de Engenharia de Requisitos | Aula de 01/09**
 
**Objetivo:** registrar as necessidades dos stakeholders e transformá-las em requisitos funcionais, requisitos de qualidade, restrições e regras de negócio, mantendo foco no que é necessário para resolver o problema.
 
---
 
## 1. Identificação do grupo
 
| Informação | Preenchimento |
|---|---|
| Turma | A |
| Nome do projeto | Gestão de Clínica e Agendamento de Consultas |
| Integrante 1 | Cauã Diniz|
| Integrante 2 |Eduardo Victor|
| Integrante 3 |Isabella Saboia|
| Integrante 4 |Lucca Peres |
| Integrante 5 |Luis Eduardo |
| Integrante 6 |Moises Cunha |
 
---
 
## 2. Contexto do projeto
 
### 2.1 Qual problema o sistema pretende resolver?
  O agendamento de consultas na clínica ainda é feito, por telefone e anotado em planilhas ou agendas físicas. 
 Na prática, isso acaba gerando vários problemas: o paciente pode ter dificuldade para conseguir contato com a clínica, podem acontecer dois agendamentos para o mesmo horário,
 algumas consultas são esquecidas por falta de lembretes e a recepção perde tempo procurando informações de pacientes e médicos.

O principal problema é a falta de uma forma única e organizada de cuidar dos agendamentos. 
Sem um sistema centralizado, fica mais difícil marcar, consultar e acompanhar as consultas, o que acaba gerando retrabalho para a equipe, mais faltas e uma experiência ruim tanto para os pacientes quanto para os profissionais.
O problema central é a falta de um processo único, confiável e acessível para marcar, consultar e gerenciar consultas médicas, o que causa retrabalho, faltas e insatisfação de pacientes e profissionais.


### 2.2 Quem é afetado pelo problema?
 Pacientes, que enfrentam dificuldade para marcar e confirmar consultas; recepcionistas, que lidam com o retrabalho de conferir e ajustar horários manualmente; médicos, que perdem tempo com agenda desorganizada ou consultas com informações incompletas; 
 e a gestão da clínica, que não tem dados consolidados sobre atendimentos, faltas e ocupação da agenda.
 
### 2.3 Como esse problema é resolvido atualmente?
 O agendamento é feito por telefone ou presencialmente, com a recepcionista anotando os horários em uma planilha eletrônica (Excel/Google Sheets) ou agenda de papel. 
 As confirmações de consulta, quando ocorrem, são feitas manualmente por telefone ou mensagens de WhatsApp na véspera do atendimento.
 
### 2.4 Quais são as principais dificuldades do processo atual?
  
1. Ocorrência de agendamentos duplicados para o mesmo médico e horário.
2. Pacientes faltam às consultas por não receberem lembretes.
3. Dificuldade da recepção em consultar rapidamente o histórico de atendimentos de um paciente.
4. Perda de tempo dos pacientes ao tentar marcar consulta por telefone em horários de alta demanda.
5. Falta de dados consolidados para a gestão acompanhar faltas, cancelamentos e ocupação da agenda.
 
### 2.5 Qual resultado se espera alcançar com o novo sistema?
 
Espera-se centralizar o agendamento de consultas em um único sistema, eliminando duplicidade de horários, reduzindo faltas por meio de lembretes automáticos, agilizando o atendimento na recepção e fornecendo à gestão relatórios confiáveis sobre o funcionamento da clínica.
 
---
 
## 3. Identificação dos stakeholders
  
| ID | Stakeholder | Papel | Necessidade/Interesse | Influência |
|---|---|---|---|---|
| ST01 | Paciente | Usuário que agenda e recebe atendimento | Marcar, remarcar e acompanhar consultas com facilidade | Alta |
| ST02 | Recepcionista | Opera o sistema no dia a dia da clínica | Gerenciar agenda e cadastro de pacientes sem retrabalho | Alta |
| ST03 | Médico/Profissional de saúde | Realiza os atendimentos | Consultar agenda e histórico do paciente antes da consulta | Alta |
| ST04 | Gestor/Administrador da clínica | Responsável pela operação e resultados da clínica | Relatórios de atendimentos, faltas e ocupação da agenda | Média |
| ST05 | Equipe de TI/Suporte | Mantém o sistema em funcionamento | Sistema estável, seguro e fácil de manter | Baixa |
 
**Stakeholder principal:** Pacientes
 
**Por quê?** 
O paciente é quem sofre diretamente as consequências do processo atual (dificuldade de contato, faltas por esquecimento, falta de confirmação) e é o motivador original do problema. 
A maioria dos requisitos funcionais existe para atender às necessidades desse stakeholder, ainda que a recepcionista seja quem opera o sistema com maior frequência
 
---
 
## 4. Perguntas para o levantamento
 
 
| Pergunta | Resposta |
|---|---|
| O que esse usuário precisa fazer? | Agendar, remarcar e cancelar consultas; consultar seus próprios agendamentos. |
| Qual problema ele enfrenta atualmente? | Dificuldade para conseguir atendimento por telefone e falta de confirmação da consulta marcada. |
| Quais informações ele precisa consultar? | Especialidades e médicos disponíveis, horários livres, status da própria consulta. |
| Quais informações ele precisa cadastrar ou alterar? | Dados pessoais, telefone de contato, convênio/plano de saúde. |
| Quais tarefas são repetitivas? | Informar os mesmos dados pessoais a cada contato com a clínica. |
| Quais tarefas consomem mais tempo? | Esperar na linha telefônica para conseguir um horário. |
| Quais erros acontecem atualmente? | Agendamento duplicado no mesmo horário; perda da informação de consulta marcada. |
| O usuário precisa receber notificações? | Sim — confirmação do agendamento e lembrete próximo à data da consulta. |
| O sistema precisará gerar documentos ou relatórios? | Sim — comprovante de agendamento. |
| Existem informações que precisam ser protegidas? | Sim — dados pessoais e de saúde, conforme a LGPD. |
| O sistema precisará se comunicar com outro sistema? | Possivelmente com serviço de envio de e-mail/SMS para notificações. |
| Existem regras que precisam obrigatoriamente ser respeitadas? | Sim — não permitir dois agendamentos no mesmo horário para o mesmo médico. |
| O que faria o usuário considerar a solução satisfatória? | Conseguir marcar uma consulta em poucos minutos, sem erros, e ser lembrado antes do atendimento. |
 
---
 
## 5. Necessidades identificadas
 
 
| ID | Stakeholder | Necessidade identificada | Problema relacionado |
|---|---|---|---|
| N01 | Paciente | Agendar consulta sem depender de telefone | Dificuldade de contato telefônico |
| N02 | Paciente | Receber lembrete da consulta marcada | Esquecimento e faltas às consultas |
| N03 | Recepcionista | Visualizar a agenda consolidada de todos os médicos | Agenda fragmentada em planilhas separadas |
| N04 | Recepcionista | Impedir agendamentos duplicados | Conflitos de horário para o mesmo médico |
| N05 | Médico | Consultar o histórico do paciente antes da consulta | Falta de acesso rápido ao histórico de atendimentos |
| N06 | Gestor | Gerar relatórios de atendimentos, faltas e cancelamentos | Falta de dados consolidados sobre a operação da clínica |
| N07 | Paciente | Cancelar ou remarcar consulta facilmente | Processo manual e demorado por telefone |
| N08 | Recepcionista | Cadastrar e atualizar dados dos pacientes | Informações desatualizadas ou dispersas |
 
---
 
## 6. Levantamento dos Requisitos Funcionais
 
| ID | Requisito Funcional | Stakeholder/Fonte | Necessidade relacionada | Prioridade |
|---|---|---|---|---|
| RF01 | O sistema deve permitir que o paciente agende uma consulta escolhendo especialidade, médico e horário disponível. | Paciente | N01 | Alta |
| RF02 | O sistema deve enviar uma notificação de lembrete ao paciente 24 horas antes da consulta. | Paciente | N02 | Alta |
| RF03 | O sistema deve impedir que dois pacientes sejam agendados no mesmo horário para o mesmo médico. | Recepcionista | N04 | Alta |
| RF04 | O sistema deve permitir que a recepcionista visualize a agenda de todos os médicos em uma única tela. | Recepcionista | N03 | Alta |
| RF05 | O sistema deve permitir que o médico consulte o histórico de atendimentos do paciente antes da consulta. | Médico | N05 | Média |
| RF06 | O sistema deve permitir que o paciente cancele ou remarque uma consulta com no mínimo 24 horas de antecedência. | Paciente | N07 | Alta |
| RF07 | O sistema deve permitir o cadastro e a atualização dos dados pessoais e do convênio do paciente. | Recepcionista | N08 | Média |
| RF08 | O sistema deve gerar um relatório de consultas realizadas, canceladas e faltas por período selecionado. | Gestor da clínica | N06 | Média |
 
---
 
## 7. Levantamento dos Requisitos de Qualidade
 
 
| ID | Característica de qualidade | Requisito mensurável | Como verificar? |
|---|---|---|---|
| RQ01 | Desempenho | O sistema deve exibir os horários disponíveis em até 3 segundos para 95% das requisições. | Teste de carga medindo tempo de resposta com múltiplos usuários simultâneos. |
| RQ02 | Segurança | Os dados pessoais e de saúde dos pacientes devem ser armazenados de forma criptografada, em conformidade com a LGPD. | Auditoria técnica verificando criptografia no banco de dados e nos canais de comunicação. |
| RQ03 | Usabilidade/Interação | Um paciente sem treinamento prévio deve conseguir concluir um agendamento em no máximo 4 telas/etapas. | Teste de usabilidade com usuários reais, contando o número de etapas até a conclusão. |
| RQ04 | Confiabilidade | O sistema deve manter disponibilidade mínima de 99% durante o horário de funcionamento da clínica (8h às 18h). | Monitoramento de uptime durante o período de funcionamento, registrado em log. |
| RQ05 | Compatibilidade/Portabilidade | O sistema deve funcionar corretamente nas duas versões mais recentes dos navegadores Chrome, Firefox e Edge, e em dispositivos Android e iOS. | Testes manuais de compatibilidade em cada navegador/dispositivo listado. |
 
---
 
## 8. Levantamento das Restrições
  
| ID | Restrição | Categoria | Justificativa/Fonte |
|---|---|---|---|
| RES01 | O sistema deve estar em conformidade com a LGPD no tratamento de dados de pacientes. | Legal | Exigência legal para armazenamento e uso de dados pessoais e de saúde. |
| RES02 | O projeto deve ser concluído até o final do semestre letivo. | Prazo | Cronograma definido pela disciplina. |
| RES03 | O sistema deve ser desenvolvido utilizando apenas ferramentas e bibliotecas gratuitas ou open source. | Custo | Ausência de orçamento para licenciamento de software no projeto acadêmico. |
 
---
 
## 9. Regras de negócio identificadas
 
| ID | Regra de negócio | Fonte |
|---|---|---|
| RN01 | Um mesmo médico não pode ter duas consultas agendadas no mesmo horário. | Recepcionista |
| RN02 | Somente pacientes cadastrados no sistema podem agendar consultas. | Gestor da clínica |
| RN03 | O cancelamento ou remarcação de consulta só é permitido com antecedência mínima de 24 horas. | Recepcionista / Gestor da clínica |
 
---
 
## 10. Matriz consolidada de requisitos
 
| ID | Descrição | Tipo | Stakeholder/Fonte | Prioridade |
|---|---|---|---|---|
| RF01 | Agendar consulta por especialidade, médico e horário | Funcional | Paciente | Alta |
| RF02 | Enviar lembrete 24h antes da consulta | Funcional | Paciente | Alta |
| RF03 | Impedir agendamento duplicado no mesmo horário | Funcional | Recepcionista | Alta |
| RF04 | Visualizar agenda consolidada de todos os médicos | Funcional | Recepcionista | Alta |
| RF06 | Cancelar/remarcar consulta com 24h de antecedência | Funcional | Paciente | Alta |
| RQ01 | Exibir horários disponíveis em até 3s (95% das requisições) | Qualidade | Todos os usuários | Alta |
| RQ02 | Criptografar dados pessoais e de saúde (LGPD) | Qualidade | Gestor / Legal | Alta |
| RES01 | Conformidade com a LGPD | Restrição | Legal | Alta |
| RES02 | Entrega até o final do semestre letivo | Restrição | Cronograma da disciplina | Alta |
| RN01 | Um médico não pode ter duas consultas no mesmo horário | Restrição | Recepcionista | Alta |
 
---
 
## 11. Revisão por pares - Caça à ambiguidade
  
| ID | Problema encontrado | Sugestão do grupo revisor |
|---|---|---|
| | | |
| | | |
| | | |
| | | |
| | | |
 
---
 
## 12. Checklist de qualidade
 
| Pergunta | Sim | Não | Observação |
|---|---|---|---|
| O requisito está completo? | ☐ | ☐ | |
| Está correto em relação à necessidade do stakeholder? | ☐ | ☐ | |
| Descreve apenas uma capacidade ou característica? | ☐ | ☐ | |
| É necessário? | ☐ | ☐ | |
| É viável? | ☐ | ☐ | |
| Possui prioridade? | ☐ | ☐ | |
| Está livre de ambiguidades? | ☐ | ☐ | |
| Pode ser verificado ou testado? | ☐ | ☐ | |
| A fonte/stakeholder está identificada? | ☐ | ☐ | |
 
---
 
## 13. Entrega da etapa - 31/08
 
Ao final da aula, o grupo deverá ter produzido: 8 requisitos funcionais (RF), 5 requisitos de qualidade (RQ), 3 restrições (RES) e 3 regras de negócio (RN), todos associados às necessidades e aos stakeholders identificados.
 
---
 
## 14. Reflexão final do grupo
 
**Qual requisito gerou mais discussão durante o levantamento e por quê?**

O RF03 gerou bastante discussão,pois pensamos apenas em bloquear dois pacientes no mesmo horário para o mesmo médico, mas surgiu a dúvida sobre encaixes de urgência e se o sistema deveria permitir alguma exceção controlada pela recepção.
Decidimos manter a regra geral (requisito 1) deixar para uma etapa futura a definição de como tratar encaixes excepcionais.


**Qual necessidade do usuário inicialmente parecia simples, mas gerou vários requisitos?**
 

A necessidade N02 parecia simples no início, mas ao debater percebemos que envolvia várias decisões: quando enviar o lembrete (RF02), o que fazer se o paciente não confirmar, e se isso deveria estar associado a uma regra de cancelamento automático em caso de não confirmação. 
Isso mostrou que uma necessidade pequena pode se transformar em múltiplos requisitos.
 
**O grupo identificou algum requisito implícito que somente apareceu durante a discussão? Qual?**

 Sim. Durante a discussão sobre RF06 (cancelamento/remarcação), percebemos que havia uma regra implícita que ninguém tinha registrado antes, o sistema precisa impedir cancelamentos de última hora (RN03), algo que os pacientes já assumiam como claro, mas que não estava explícito em nenhuma necessidade. 
 Isso só veio à tona quando discutimos o que aconteceria se um paciente tentasse cancelar poucas horas antes da consulta.

 
---
 
*Orientação: nesta etapa, o foco não é projetar telas nem escolher tecnologias. O objetivo é compreender e registrar o que é necessário para resolver o problema, mantendo os requisitos claros, verificáveis e rastreáveis às necessidades dos stakeholders.*
