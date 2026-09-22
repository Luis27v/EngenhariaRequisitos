<div align = "center">

Atividade 01 

Isabella Saboia

UniCEUB 
# Atividade 01 - Engenharia de Requisitos


**Situação Problema**:
---

- Desafio - Problema
- Escola necessitando sistema de controle de alunos
- Levantamento de Requisitos

--- 


**Perguntas**
<div align = "left">

1. **Quem utilizará o sistema?**
+ O sistema será utilizado por uma escola com o objetivo final de controlar o acesso e a saída de seus alunos ao ambiente escolar.
  Os principais usuários são: **alunos** (que terão o acesso registrado), **porteiros** (que operam o controle de entrada e saída), **secretaria e diretores** (que cadastram alunos e consultam relatórios) e, indiretamente, **responsáveis/pais** (que podem ser notificados sobre o acesso do aluno).
  
2. **Requisitos funcionais do Sistema:**
+ O sistema deve controlar o acesso e a saída dos alunos no ambiente escolar, registrando data e horário de cada movimentação.
+ O sistema deve permitir o controle de acesso por meio de carteirinha digital ou reconhecimento facial (FaceID).
+ O sistema deve permitir o cadastro de alunos por atores administrativos (diretores, secretaria, porteiros).
+ O sistema deve gerar relatórios com a quantidade de alunos que acessaram a escola diariamente.
+ O sistema deve lançar automaticamente as faltas dos alunos com base no horário de registro de acesso.
+ O sistema deve notificar o responsável quando o aluno registrar entrada ou saída fora do horário esperado.

  
3. **Requisitos Não-funcionais do Sistema:**
 
+ **Desempenho:** o sistema deve registrar o acesso do aluno (leitura da carteirinha/FaceID) em até 2 segundos, mesmo em horários de pico de entrada e saída.
+ **Segurança:** os dados cadastrais e biométricos dos alunos devem ser armazenados de forma criptografada, e o acesso às informações deve ser restrito por perfil de usuário (aluno, porteiro, secretaria, diretor).
+ **Confiabilidade:** o sistema deve estar disponível durante todo o horário de funcionamento da escola, com disponibilidade mínima de 99%.
+ **Usabilidade:** um porteiro sem treinamento prévio deve conseguir registrar um acesso manual (em caso de falha do FaceID/carteirinha) em, no máximo, 3 etapas.
+ **Compatibilidade:** o sistema deve funcionar tanto em computadores da secretaria quanto em tablets/leitores utilizados na portaria.


4. **Explique, em poucas palavras, por que é importante levantar os requisitos antes de desenvolver um software.**
+ Levantar os requisitos antes de desenvolver o software é importante porque garante clareza sobre o que realmente precisa ser construído, evitando retrabalho, mal-entendidos entre a equipe e o cliente, e funcionalidades desnecessárias ou faltantes. Um bom levantamento também permite identificar não só o que o sistema deve fazer (requisitos funcionais), mas também com qual qualidade ele deve fazer isso (requisitos não funcionais), tornando o produto final mais elaborado, seguro e alinhado às reais necessidades da escola.
 
