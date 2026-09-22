# Revisão 01 — Engenharia de Requisitos

*Material de revisão: Levantamento de Requisitos, ISO/IEC 25010, BPM CBOK, BABOK e MoSCoW.*

---

## 1. O que é Engenharia de Requisitos

É a área que se ocupa de **descobrir, analisar, documentar e gerenciar** as necessidades dos stakeholders, transformando-as em requisitos claros, verificáveis e rastreáveis, que orientam a construção de um sistema.

**Ideia central:** o levantamento de requisitos **não começa pelas telas do sistema**. Antes de definir funcionalidades, é preciso compreender o negócio, os processos, os stakeholders, as regras, os problemas e os objetivos da organização.

### Ciclo básico do levantamento
```
Problema / Necessidade
        ↓
Identificação dos Stakeholders
        ↓
Levantamento das Necessidades
        ↓
Requisitos Funcionais, de Qualidade, Restrições e Regras de Negócio
        ↓
Priorização
        ↓
Revisão (caça à ambiguidade) e Validação
```

---

## 2. Stakeholders

**Definição (BABOK):** qualquer indivíduo ou grupo com interesse ou que pode ser afetado por uma mudança ou solução — não se limita a quem paga ou desenvolve o sistema.

Para cada stakeholder, vale investigar:
- O que ele precisa fazer?
- Que informações consulta, cadastra ou altera?
- Quais tarefas são repetitivas ou consomem mais tempo?
- Que erros ocorrem hoje?
- Precisa de notificações, relatórios, integração com outro sistema?
- Existem regras obrigatórias e informações sensíveis?

**Stakeholder principal:** normalmente aquele cuja necessidade motiva o problema central (ex.: o paciente, no caso da clínica).

---

## 3. Tipos de requisitos

### 3.1 Segundo a prática de Engenharia de Requisitos

| Tipo | O que é | Exemplo |
|---|---|---|
| **Requisito Funcional (RF)** | Descreve uma capacidade/ação que o sistema deve executar | RF01 — O sistema deverá permitir cadastrar pacientes. |
| **Requisito de Qualidade / Não Funcional (RQ/RNF)** | Descreve uma característica de qualidade, mensurável e verificável | RNF01 — O sistema deverá exibir os horários em até 3s para 95% das requisições. |
| **Restrição** | Limitação de tecnologia, prazo, custo, legal ou de processo | Sistema deve estar em conformidade com a LGPD. |
| **Regra de Negócio (RN)** | Política ou norma do domínio que restringe/define o negócio | Um médico não pode ter dois pacientes agendados no mesmo horário. |

### 3.2 Segundo o BABOK (4 categorias)

| Categoria | Definição |
|---|---|
| **Business Requirements** (Negócio) | Objetivos de alto nível — o "porquê" do projeto. |
| **Stakeholder Requirements** | Necessidades de um stakeholder específico; ponte entre negócio e solução. |
| **Solution Requirements** | Capacidades da solução — dividem-se em **funcionais** e **não funcionais**. |
| **Transition Requirements** | Capacidades necessárias apenas durante a mudança do estado atual para o futuro (ex.: migração de dados, treinamento). |

**Técnicas de elicitação (BABOK):** entrevista, workshop, observação, questionário, prototipagem, análise de documentos.

**Rastreabilidade (traceability):** ligar cada requisito à sua origem (necessidade/stakeholder) e a outros artefatos (testes, regras de negócio), permitindo avaliar o impacto de mudanças.

---

## 4. De requisito vago a requisito verificável

Termos como **rápido, seguro, fácil de usar, robusto, adequado, moderno** são vagos e não podem ser testados.

**Estrutura recomendada:**
> O sistema deverá **[comportamento/propriedade]**, sob **[condições]**, atingindo **[valor/limite]**, verificado por **[método de avaliação]**.

| Vago | Verificável |
|---|---|
| O sistema deve ser rápido. | O sistema deverá concluir a consulta em até 2 segundos para 95% das requisições, com até 500 usuários simultâneos. |
| O sistema deve ser fácil de usar. | Em teste com usuários, 90% dos estudantes deverão concluir a matrícula sem ajuda em até 5 minutos. |
| O sistema deve ser seguro. | Após 5 tentativas de login inválidas, a conta deve ser bloqueada por 15 minutos e o evento registrado. |

---

## 5. ISO/IEC 25010:2023 — Modelo de qualidade de produto

Pertence à família **SQuaRE** (Systems and Software Quality Requirements and Evaluation). Define **9 características de qualidade**:

| Característica | Pergunta orientadora |
|---|---|
| **Adequação funcional** | O produto fornece corretamente as funções necessárias? |
| **Eficiência de desempenho** | Responde adequadamente com os recursos disponíveis (tempo de resposta, carga)? |
| **Compatibilidade** | Convive e troca informações com outros produtos? |
| **Capacidade de interação** | As pessoas conseguem interagir bem com o produto (usabilidade)? |
| **Confiabilidade** | Permanece funcionando conforme esperado (disponibilidade, recuperação)? |
| **Segurança** | Dados, identidades e operações estão protegidos? |
| **Manutenibilidade** | Pode ser analisado, testado e modificado com eficiência? |
| **Flexibilidade** | Pode ser adaptado, instalado, substituído ou escalado? |
| **Proteção contra riscos (*safety*)** | Reduz riscos de dano a pessoas, patrimônio ou ambiente? |

> **Qualidade ≠ ausência de erros.** Um sistema pode executar corretamente suas funções e ainda ter problemas de desempenho, acessibilidade, segurança, manutenibilidade ou adaptação.

---

## 6. BPM e BPM CBOK

**Processo de negócio:** conjunto de atividades executadas por pessoas ou sistemas para gerar um resultado que entrega valor a um cliente.

**Ponta a ponta (end-to-end):** o processo deve ser analisado do evento que o inicia até a entrega de valor final, mesmo que atravesse vários setores — evita a análise em "silos".

### Perguntas de mapeamento de processo (5W2H adaptado)
- **Quem?** cliente, executores, gestor, quem fornece informação/participa das decisões.
- **O quê?** entradas, saídas, recursos, ferramentas, problemas, pontos positivos, indicadores.
- **Quando?** início, execução das atividades, término.
- **Onde?** onde inicia, onde é executado, onde é registrado.
- **Por quê?** motivo de existir, valor entregue ao cliente e à organização.
- **Como?** como é executado, registrado, comunicado hoje.

### AS-IS x TO-BE

| AS-IS | TO-BE |
|---|---|
| Processo **atual**, como realmente é executado, com problemas e gargalos. | Processo **futuro**, redesenhado com as melhorias propostas e apoio do sistema. |

### Ciclo de vida do BPM
```
Planejamento → Análise → Desenho e Modelagem → Implementação → Monitoramento e Controle → Refinamento
```
(processo cíclico, volta ao início para melhoria contínua)

### Indicadores de desempenho (exemplos)
Taxa de ocupação da agenda, quantidade de consultas realizadas, taxa de cancelamento, taxa de faltas, tempo médio de atendimento.

---

## 7. MoSCoW — Priorização de requisitos

| Categoria | Significado |
|---|---|
| **Must Have** | Obrigatório — sem ele a solução não é viável. |
| **Should Have** | Importante, mas a solução pode ser entregue sem ele (com alguma limitação). |
| **Could Have** | Desejável, impacto pequeno se ficar de fora. |
| **Won't Have (this time)** | Não entra nesta versão, mas pode ser reconsiderado no futuro. |

> Toda decisão de priorização deve ser **justificada** (ex.: risco, custo, dependência de outro requisito, urgência do stakeholder).

---

## 8. Checklist de qualidade de um requisito

Um bom requisito deve ser:

- [ ] **Completo**
- [ ] **Correto** em relação à necessidade do stakeholder
- [ ] **Atômico** (descreve apenas uma capacidade/característica)
- [ ] **Necessário**
- [ ] **Viável**
- [ ] **Priorizado**
- [ ] **Livre de ambiguidades**
- [ ] **Verificável/testável**
- [ ] Com **fonte/stakeholder identificado**

---

## 9. Modelo mental para a prova

Ao ler qualquer questão, pergunte:

1. **É sobre o que o sistema faz?** → Requisito Funcional.
2. **É sobre uma qualidade/característica (desempenho, segurança, usabilidade...)?** → Requisito de Qualidade/Não Funcional → veja qual das 9 características da ISO 25010 se encaixa.
3. **É uma limitação externa (prazo, custo, tecnologia, lei)?** → Restrição.
4. **É uma política/norma do domínio que "trava" um comportamento?** → Regra de Negócio.
5. **É sobre prioridade de entrega?** → MoSCoW (Must/Should/Could/Won't).
6. **É sobre o processo de negócio em si (antes do sistema existir)?** → BPM CBOK (AS-IS, TO-BE, ponta a ponta, ciclo de vida).
7. **É sobre categorias amplas de requisitos (negócio, stakeholder, solução, transição) ou técnicas de elicitação?** → BABOK.

---

## 10. Termos que costumam confundir

| Termo | Não confundir com |
|---|---|
| Requisito Funcional | Regra de Negócio (a regra restringe; o requisito descreve uma capacidade) |
| Requisito Não Funcional | Restrição (não funcional é sobre qualidade do produto; restrição é sobre condições externas ao produto) |
| AS-IS | TO-BE (atual x futuro) |
| Segurança (ISO 25010) | *Safety*/Proteção contra riscos (dados x integridade física) |
| Must Have (MoSCoW) | Requisito Funcional obrigatório por natureza — MoSCoW é sobre *prioridade de entrega*, não sobre o tipo do requisito |
| Stakeholder Requirements (BABOK) | Requisitos Funcionais (stakeholder requirement é a necessidade; o requisito funcional é a tradução técnica dela) |
