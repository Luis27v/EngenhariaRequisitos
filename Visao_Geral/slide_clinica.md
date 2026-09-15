# SISTEMA DE GESTÃO PARA CLÍNICA MÉDICA

> Solução estruturada de software para otimização de atendimentos e gestão em saúde

## Integrantes do Projeto

- Cauã Diniz
- Eduardo Victor
- Isabella Saboia
- Lucca Peres
- Luis Eduardo
- Moisés Cunha


---

# 1. Problemas & Impactos Clínicos

## Sistema de Gestão de Clínica | Diagnóstico de Problemas

### Nota Gerencial

A ausência de um sistema integrado gera retrabalho receptivo, reduz o tempo efetivo de consulta e expõe a clínica a riscos com a LGPD e o Conselho Federal de Medicina.

## Gargalos Operacionais da Clínica

- **Agendamento Disperso:** Controle em papel e planilhas com choques de horário.
- **Alto No-Show:** Faltas frequentes por ausência de lembretes automáticos.
- **Prontuários Físicos:** Dificuldade de acesso, busca lenta e risco de perda.
- **Filas na Recepção:** Demora na triagem e na validação de convênios/guias.

## Impactos Diretos nos Serviços

- **Tempo Médico Ocioso:** Horários vagos não reutilizados por cancelamentos tardios.
- **Experiência do Paciente:** Atrasos frequentes e insatisfação na sala de espera.
- **Faturamento & Convênios:** Glosas médicas e falta de previsão financeira.


---

# 2. Stakeholders & Papel do Analista

## Sistema de Gestão de Clínica | Mapeamento de Stakeholders

### Ciclo de Engenharia de Requisitos

1. **Diagnóstico**
2. **Envolvidos**
3. **Elicitação**
4. **Mapeamento**
5. **Requisitos**
6. **Escopo MVP**
7. **Validação**

## Stakeholders

| Papel / Nível | Stakeholder | Interesse Principal | Responsabilidade Chave |
|---|---|---|---|
| **Diretoria** | Diretor Médico / Gestor | Sustentabilidade e reputação da clínica | Aprovar orçamento e diretrizes do sistema |
| **Corpo Clínico** | Médicos / Especialistas | Prontuário ágil e histórico completo | Registro técnico de consultas e diagnósticos |
| **Operacional** | Recepcionistas / Secretárias | Agendamento fluido e recepção rápida | Cadastrar pacientes e gerenciar salas de espera |
| **Cliente Final** | Pacientes | Praticidade ao agendar e pontualidade | Fornecer dados cadastrais e comparecer |
| **Facilitador** | Analista de Negócios | Traduzir rotinas médicas em requisitos | Especificar, modelar e validar a solução |


---

# 3. Business Needs & Elicitação

## Sistema de Gestão de Clínica | Elicitação BABOK

## Necessidades da Clínica

- **Agendamento Unificado:** Grade médica centralizada e sem sobramarcação.
- **Redução do No-Show:** Confirmação e lembretes via WhatsApp/SMS.
- **Prontuário Eletrônico (PEP):** Histórico médico seguro e acessível.
- **Gestão de Convênios:** Emissão simplificada de guias TISS.
- **Triagem de Espera:** Controle do fluxo recepção-consultório.

## Técnicas de Elicitação Aplicadas

- **Entrevistas:** Entendimento das rotinas de médicos e secretárias.
- **Observação Direta:** Acompanhamento do atendimento presencial.
- **Workshops:** Alinhamento entre médicos e gestores para o PEP.
- **Análise Documental:** Análise de fichas físicas, receitas e guias TISS.
- **Questionários:** Mapeamento do tempo de espera dos pacientes.


---

# 4. Especificação de Requisitos

## Sistema de Gestão de Clínica | Requisitos Funcionais

## Módulo 01: Recepção & Agendamento

- **RF01 - Cadastro de Pacientes:** Registro de dados, contatos e plano de saúde.
- **RF02 - Agenda Médica:** Marcação, remarcação e encaixes por médico.
- **RF03 - Confirmação Automática:** Disparo de lembretes via WhatsApp.
- **RF04 - Controle de Espera:** Chamada de pacientes para a sala médica.
- **RF05 - Gestão de Guias:** Validação de autorizações de convênio.

## Módulo 02: Atendimento Médico & Gestão

- **RF06 - Prontuário Eletrônico:** Anamnese, diagnóstico e histórico clínico.
- **RF07 - Prescrição Digital:** Emissão de receitas e atestados com assinatura.
- **RF08 - Anexo de Exames:** Upload de laudos e exames em PDF/imagem.
- **RF09 - Faturamento:** Apuração de consultas e repasse aos médicos.
- **RF10 - Indicadores:** Dashboards de ocupação, faltas e receita.


---

# 5. Requisitos Não Funcionais & RN

## Atributos de Qualidade (RNF)

- **Usabilidade:** Interface ágil para médicos preencherem em < 3 minutos.
- **Segurança & LGPD:** Criptografia end-to-end e dados sensíveis protegidos.
- **Conformidade CFM:** Aderência às diretrizes de Prontuário Eletrônico.
- **Desempenho:** Resposta do prontuário em menos de 2 segundos.
- **Disponibilidade:** SLA de 99.9% para garantir a operação diária.

## Regras de Negócio (RN)

- **RN01:** Somente o médico atendente acessa o prontuário do paciente.
- **RN02:** Proibido agendamento sobreposto para o mesmo profissional.
- **RN03:** Prontuário assinado torna-se imutável, aceitando apenas adendos.
- **RN04:** Cancelamentos em < 24h notificam a lista de espera.
- **RN05:** Prescrição de controlados exige certificado digital ICP-Brasil.


---

# 6. Priorização do MVP Clínico

## Sistema de Gestão de Clínica | Qualidade de Requisitos

## Eliminação de Ambiguidades de Requisitos

### Alta Prioridade (MVP)

**RF01-RF07, RNF (LGPD/CFM/Usabilidade) e RN01-RN05.**

Foco em:

- Agendamento
- Lembrete
- Prontuário Básico

### Média Prioridade

**RF08-RF09**

- Anexo de laudos em PDF/imagem
- Módulo de faturamento com repasse médico

### Baixa Prioridade (Futuro)

- Telemedicina integrada
- IA de apoio ao diagnóstico
- Agendamento online direto pelo paciente

## Exemplos de Eliminação de Ambiguidades

### Requisito Ambíguo 01

> "O prontuário deve ser rápido de preencher."

**Requisito Ajustado:**

> Abertura em < 2s e preenchimento da anamnese com até 5 cliques usando modelos padrão.

### Requisito Ambíguo 02

> "O sistema deve diminuir as faltas de pacientes."

**Requisito Ajustado:**

> Disparo de mensagens no WhatsApp 48h e 24h antes, com confirmação via 1 toque.


---

# 7. Benefícios & Reflexões

## Sistema de Gestão de Clínica | Valor Entregue

## Benefícios Diretos para a Clínica

- Queda expressiva no índice de faltas (no-show) de pacientes.
- Agilidade no atendimento e redução no tempo de espera.
- Eliminação de papel e ganho de espaço físico.
- Conformidade jurídica com LGPD e normas do CFM.
- Aumento no aproveitamento e faturamento das agendas.

## Reflexões da Equipe de Projeto

- **Sensibilidade dos Dados:** Informações de saúde exigem rigor absoluto em LGPD e privacidade.
- **Usabilidade Médica:** O médico precisa focar no paciente; a interface deve ser limpa e rápida.
- **Gestão do Tempo:** Automação da confirmação resolve a principal dor financeira da clínica.


---

# 8. Fluxo BABOK & Conclusão

## Fluxo BABOK

### 1. Gargalo Clínico

Identificação dos principais problemas e gargalos existentes na clínica.

### 2. Elicitação

Levantamento das necessidades e expectativas dos stakeholders.

### 3. Análise & Doc

Análise, documentação e transformação das necessidades em requisitos.

### 4. MVP Clínico

Definição das funcionalidades prioritárias para a primeira versão da solução.

### 5. Validação

Validação dos requisitos e da solução junto aos envolvidos.

### 6. Implantação

Implementação da solução no ambiente da clínica.

### 7. Valor em Saúde

Geração de valor por meio de um atendimento mais eficiente, seguro e organizado.


## Engenharia de Requisitos Garantindo Eficiência no Atendimento Médico

A aplicação sistemática das diretrizes do BABOK permitiu transformar os problemas operacionais da clínica em um software seguro, eficiente e totalmente aderente à legislação médica e de proteção de dados.

### Resultado

**Problema Clínico → Requisitos → MVP → Valor para a Saúde**
