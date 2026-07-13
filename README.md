# Projeto Agendamento de Consultas — Gestão de Riscos e Comunicação com Apoio de IA Generativa

## Descrição do projeto

Este repositório reúne os artefatos produzidos para o **exercício prático da Unidade III — Riscos, Comunicação e Documentação Inteligente**, do curso *Gerência de Projetos de Software Apoiada por Inteligência Artificial Generativa* (AKCIT / UFG / Embrapii).

O cenário utilizado é o **estudo de caso proposto no curso**: um aplicativo móvel para **agendamento de consultas médicas**, com funcionalidades de cadastro de usuários, gestão de agenda médica, agendamento de consultas, notificações e integração com um sistema externo de prontuário.

O projeto encontra-se em **fase intermediária de desenvolvimento** e, nas últimas semanas, enfrenta três desafios principais:

- Instabilidade na **integração com o sistema de prontuário** (API sem documentação clara e mudanças recentes no sistema externo);
- **Mudanças de requisitos** solicitadas por stakeholders no fluxo de agendamento (novas validações e regras de negócio);
- **Sobrecarga da equipe** (4 desenvolvedores e 1 tester), com dificuldade de cumprir os prazos inicialmente estimados.

A integração com o sistema externo é **crítica** para a entrega do projeto.

## Objetivo do exercício

Aplicar, de forma prática, o processo de **gerenciamento de riscos** (identificação → análise → resposta) e a **comunicação com stakeholders**, utilizando **IA Generativa (LLMs)** como ferramenta de apoio à identificação, estruturação e redação — mantendo a validação e o julgamento sob responsabilidade humana.

## Organização do repositório

```
projeto-agendamento-consultas/
├── README.md                        # este arquivo
├── riscos/
│   ├── identificacao.md             # Etapa 1 — riscos identificados
│   ├── analise.md                   # Etapa 2 — análise qualitativa (probabilidade x impacto)
│   └── respostas.md                 # Etapa 3 — estratégias de resposta
└── comunicacao/
    └── status-stakeholders.md       # Etapa 4 — comunicação para stakeholders
```

- **`riscos/identificacao.md`** — lista de riscos, descrição e contexto de ocorrência.
- **`riscos/analise.md`** — análise estruturada (impactos, fatores condicionantes, probabilidade/impacto qualitativos) e matriz de riscos.
- **`riscos/respostas.md`** — estratégia (evitar / mitigar / transferir / aceitar) por risco, com justificativa e ações.
- **`comunicacao/status-stakeholders.md`** — comunicado de status em linguagem acessível, com foco em tomada de decisão.

## Uso de IA Generativa

Todos os artefatos foram produzidos com apoio de um LLM, seguindo os prompts estruturados (persona, tarefa, contexto, saída, restrições
