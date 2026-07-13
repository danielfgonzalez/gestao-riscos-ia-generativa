# Etapa 3 — Definição de Estratégias de Resposta

> **Apoio de IA:** estratégias exploradas com apoio de um LLM (persona de *gerente de projetos com experiência em resposta a riscos*). A **escolha final** de cada estratégia considerou o contexto, as restrições e o apetite ao risco do projeto, sob responsabilidade da equipe.

Estratégias consideradas: **evitar**, **mitigar**, **transferir**, **aceitar**. Abaixo, a estratégia escolhida para cada risco prioritário, com justificativa e ações.

---

## R1 — Instabilidade na integração com o prontuário *(prioridade máxima)*
- **Estratégia escolhida:** **Mitigar**
- **Justificativa:** não é possível evitar a integração (é crítica para a entrega) nem transferi-la integralmente; resta reduzir probabilidade e impacto das falhas.
- **Ações:**
  - Implementar uma **camada de abstração (adapter/anti-corruption layer)** para isolar o app das mudanças do sistema externo;
  - Criar **testes de contrato** e um **ambiente de mock/sandbox** da API para desenvolver sem depender da disponibilidade do fornecedor;
  - Adicionar **tratamento de erros, timeouts e retentativas**, com mensagens claras ao usuário;
  - Estabelecer **canal formal de comunicação** com o fornecedor para antecipar mudanças.

## R4 — Sobrecarga da equipe / atraso de cronograma *(prioridade máxima)*
- **Estratégia escolhida:** **Mitigar**
- **Justificativa:** o risco não pode ser aceito (afeta prazo e qualidade) nem eliminado; deve ser reduzido por repriorização e ajuste de escopo.
- **Ações:**
  - **Repriorizar o backlog** com stakeholders, focando no que é essencial para a entrega (MVP);
  - **Repactuar prazos** de forma transparente com base no impacto das mudanças;
  - Redistribuir tarefas e reduzir trabalho em paralelo (limitar WIP);
  - Reavaliar a necessidade de **reforço temporário** de equipe para o QA e a integração.

## R2 — Documentação de API insuficiente
- **Estratégia escolhida:** **Mitigar**
- **Justificativa:** a documentação não depende da equipe, mas seu impacto pode ser reduzido internamente.
- **Ações:** produzir **documentação interna** da API à medida que é compreendida; centralizar o conhecimento (não concentrar em uma só pessoa); registrar exemplos de requisições/respostas.

## R3 — Mudanças frequentes de requisitos
- **Estratégia escolhida:** **Mitigar**
- **Justificativa:** mudanças são inevitáveis em software; o foco é controlá-las, não impedi-las.
- **Ações:** implantar um **processo leve de controle de mudanças** (avaliação de impacto em prazo/esforço antes de aceitar); trabalhar em **ciclos curtos** com validação frequente; manter os requisitos versionados no repositório.

## R5 — Gargalo de QA
- **Estratégia escolhida:** **Mitigar**
- **Justificativa:** com equipe enxuta, é preciso ampliar a capacidade de teste sem depender só do headcount.
- **Ações:** introduzir **testes automatizados** para regressão; priorizar QA nas funcionalidades críticas (agendamento e integração); envolver desenvolvedores em testes de unidade.

## R6 — Dependência de fornecedor externo
- **Estratégia escolhida:** **Transferir** (complementada por mitigação)
- **Justificativa:** parte da responsabilidade é do fornecedor; formalizar essa responsabilidade reduz a exposição da equipe.
- **Ações:** estabelecer/rever **SLA e garantias contratuais** com o fornecedor; definir responsabilidades e prazos de suporte; manter a camada de abstração de R1 como proteção técnica.

## R7 — Scope creep
- **Estratégia escolhida:** **Mitigar**
- **Justificativa:** o acúmulo de mudanças é controlável com governança de escopo.
- **Ações:** vincular toda nova solicitação a uma **avaliação formal de impacto**; manter backlog priorizado e transparente; comunicar trade-offs (o que entra x o que sai/atrasa).

## R8 — Dados sensíveis / conformidade
- **Estratégia escolhida:** **Mitigar** (com possível **transferência** de partes via infraestrutura especializada)
- **Justificativa:** impacto severo justifica prevenção, mesmo com probabilidade baixa.
- **Ações:** aplicar **criptografia em trânsito e repouso**, controle de acesso e minimização de dados; revisar conformidade com LGPD; usar provedores/ambientes que ofereçam garantias de segurança.
  > ⚠️ *Requer validação com a organização quanto às exigências legais aplicáveis.*

---

**Estratégia que considero mais importante para o projeto:** a **mitigação de R1** por meio da camada de abstração + mocks/testes de contrato. Ela ataca a dependência mais crítica (integração com o prontuário), reduz o efeito em cascata sobre prazo (R4), esforço (R2) e qualidade (R5), e diminui a exposição à dependência do fornecedor (R6) — sendo, portanto, a de maior efeito alavancado no conjunto de riscos.
