# Etapa 1 — Identificação de Riscos

> **Apoio de IA:** os riscos abaixo foram levantados com apoio de um LLM (persona de *especialista em gerenciamento de riscos em projetos de software*), a partir da descrição do cenário. As sugestões foram revisadas e contextualizadas manualmente para o projeto de agendamento de consultas médicas.

## Riscos identificados

### R1 — Falha/instabilidade na integração com o sistema de prontuário
- **Descrição:** a integração com o sistema externo de prontuário apresenta instabilidade, agravada pela ausência de documentação clara da API e por mudanças recentes no sistema externo.
- **Contexto de ocorrência:** durante o consumo da API em ambiente de desenvolvimento/homologação, especialmente quando o fornecedor altera contratos, endpoints ou formatos de resposta sem aviso prévio.

### R2 — Documentação de API insuficiente ou desatualizada
- **Descrição:** falta de documentação confiável da API do prontuário obriga a equipe a trabalhar por tentativa e erro, aumentando esforço e a chance de implementações incorretas.
- **Contexto de ocorrência:** ao implementar ou manter funcionalidades dependentes do prontuário; sempre que surgem dúvidas sobre parâmetros, autenticação ou regras do sistema externo.

### R3 — Mudanças frequentes de requisitos no fluxo de agendamento
- **Descrição:** stakeholders solicitaram novas validações e regras de negócio no fluxo de agendamento, com potencial de novas mudanças ao longo do tempo.
- **Contexto de ocorrência:** em reuniões de alinhamento e revisões com stakeholders, sobretudo quando regras não foram totalmente definidas no início do projeto.

### R4 — Sobrecarga da equipe e risco de atraso no cronograma
- **Descrição:** a equipe (4 desenvolvedores e 1 tester) relatou aumento da carga de trabalho e dificuldade para cumprir prazos estimados.
- **Contexto de ocorrência:** ao acumular retrabalho de integração e mudanças de escopo simultaneamente, comprometendo as estimativas iniciais.

### R5 — Gargalo de qualidade (QA) por equipe de teste reduzida
- **Descrição:** com apenas 1 tester para toda a aplicação, há risco de a cobertura de testes ficar insuficiente, deixando defeitos passarem para produção.
- **Contexto de ocorrência:** em picos de entrega, quando várias funcionalidades chegam ao QA ao mesmo tempo, ou quando mudanças de requisitos exigem reteste.

### R6 — Dependência de fornecedor externo fora do controle da equipe
- **Descrição:** parte do sucesso do projeto depende de um sistema de prontuário mantido por terceiros, cujas mudanças e disponibilidade a equipe não controla.
- **Contexto de ocorrência:** quando o fornecedor promove alterações, indisponibilidades ou não responde a solicitações de suporte em tempo hábil.

### R7 — Comprometimento de escopo/prazo pelo acúmulo de mudanças (scope creep)
- **Descrição:** a soma de novas regras de negócio sem repactuação de prazo pode expandir o escopo de forma não controlada.
- **Contexto de ocorrência:** quando novas solicitações são incorporadas sem avaliação de impacto em prazo, esforço e prioridade.

### R8 — Sensibilidade e conformidade de dados de saúde
- **Descrição:** o app lida com dados médicos sensíveis; falhas de tratamento ou exposição podem gerar impactos legais e de reputação (ex.: LGPD).
- **Contexto de ocorrência:** no armazenamento, trânsito e integração de dados de pacientes com o sistema de prontuário.
  > ⚠️ *Necessita validação:* o nível de exigência de conformidade depende de informações não detalhadas no cenário e deve ser confirmado com a organização.

---

*Observação: os riscos identificados por um LLM são generalizações baseadas em seu treinamento e não substituem a análise da equipe. Esta lista foi revisada e priorizada com base no contexto real do projeto.*
