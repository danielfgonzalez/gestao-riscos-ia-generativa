# Etapa 2 — Análise dos Riscos

> **Apoio de IA:** análise estruturada com apoio de um LLM (persona de *analista de riscos em projetos de software*). As classificações qualitativas de probabilidade e impacto foram **definidas e validadas pela equipe** (não delegadas ao modelo), conforme orientação da Unidade III. Não são usados valores numéricos.

## Análise estruturada dos riscos

### R1 — Instabilidade na integração com o prontuário
- **Possíveis impactos:** bloqueio de funcionalidades críticas, retrabalho, atraso na entrega, perda de confiança do cliente.
- **Fatores que influenciam a ocorrência:** ausência de documentação, mudanças no sistema externo, falta de ambiente estável de testes.
- **Probabilidade:** Alta · **Impacto:** Alto
- **Justificativa:** o problema já está ocorrendo e afeta uma dependência declarada como crítica para a entrega.

### R2 — Documentação de API insuficiente
- **Possíveis impactos:** aumento de esforço, implementações incorretas, ampliação do tempo de desenvolvimento.
- **Fatores:** maturidade/colaboração do fornecedor; canais de suporte disponíveis.
- **Probabilidade:** Alta · **Impacto:** Médio
- **Justificativa:** condição atual conhecida; impacto relevante, porém contornável com engenharia reversa e testes.

### R3 — Mudanças frequentes de requisitos
- **Possíveis impactos:** retrabalho, instabilidade de escopo, desgaste da equipe, atraso.
- **Fatores:** requisitos imaturos no início; múltiplos stakeholders; ausência de processo formal de controle de mudanças.
- **Probabilidade:** Alta · **Impacto:** Médio
- **Justificativa:** já ocorreu e tende a se repetir; impacto gerenciável se houver controle de mudanças.

### R4 — Sobrecarga da equipe / atraso de cronograma
- **Possíveis impactos:** atraso nas entregas, queda de qualidade, burnout, rotatividade.
- **Fatores:** acúmulo de retrabalho e mudanças simultâneas; equipe enxuta; estimativas iniciais otimistas.
- **Probabilidade:** Alta · **Impacto:** Alto
- **Justificativa:** sintoma já relatado pela equipe, com efeito direto em prazo e qualidade.

### R5 — Gargalo de QA (1 tester)
- **Possíveis impactos:** defeitos em produção, retrabalho, impacto em dados sensíveis de saúde.
- **Fatores:** relação testes/entregas; ausência de automação; picos de entrega.
- **Probabilidade:** Média · **Impacto:** Alto
- **Justificativa:** capacidade limitada de QA frente a um domínio sensível.

### R6 — Dependência de fornecedor externo
- **Possíveis impactos:** bloqueios fora do controle da equipe, atrasos, indisponibilidade.
- **Fatores:** SLA e responsividade do fornecedor; existência de contrato/garantias.
- **Probabilidade:** Média · **Impacto:** Alto
- **Justificativa:** baixo controle sobre um componente crítico.

### R7 — Scope creep (acúmulo de mudanças)
- **Possíveis impactos:** estouro de prazo e esforço; comprometimento das entregas prioritárias.
- **Fatores:** ausência de repactuação de prazo a cada mudança; priorização informal.
- **Probabilidade:** Média · **Impacto:** Médio
- **Justificativa:** risco crescente se as mudanças não forem formalmente avaliadas.

### R8 — Dados sensíveis / conformidade
- **Possíveis impactos:** sanções legais (LGPD), danos de reputação, perda de confiança.
- **Fatores:** práticas de segurança adotadas; requisitos regulatórios (a confirmar).
- **Probabilidade:** Baixa · **Impacto:** Alto
- **Justificativa:** probabilidade menor com boas práticas, mas impacto severo se ocorrer.
  > ⚠️ *Classificação sujeita a validação com a organização quanto às exigências regulatórias.*

## Matriz Qualitativa de Riscos

| Probabilidade \ Impacto | Baixo | Médio          | Alto                 |
| ----------------------- | ----- | -------------- | -------------------- |
| **Alta**                |       | R2, R3         | R1, R4               |
| **Média**               |       | R7             | R5, R6               |
| **Baixa**               |       |                | R8                   |

**Prioridade de tratamento (mais críticos primeiro):** R1 e R4 (Alta/Alto) → R2 e R3 (Alta/Médio) → R5 e R6 (Média/Alto) → R7 (Média/Médio) → R8 (Baixa/Alto, monitorar).

---

*As classificações são qualitativas e exploratórias, sujeitas a revisão contínua ao longo do ciclo de vida do projeto.*
