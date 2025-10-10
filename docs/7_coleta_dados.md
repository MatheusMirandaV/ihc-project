## Identificação de Necessidades dos Usuários e Requisitos de IHC

### 1) Que dados coletar
- **Custos por provedor**: preço/h da VM, armazenamento (GB/mês), tráfego (GB), egress/ingress e descontos/tiers
- **Desempenho/eficiência**: latência/tempo de resposta (quando disponível), disponibilidade/SLA e famílias de instância, regiões.
- **Indicadores ambientais**: PUE, % de energia renovável, metas públicas de carbono/ESG e emissões estimadas por região.
- **Metadados de coleta**: provedor, serviço (IaaS/PaaS/SaaS), região, data/hora e fonte (API vs. scraping).
- **Telemetria opcional do dashboard (com consentimento)**: filtros mais usados, tarefas concluídas e erros.

### 2) De quem coletar
- **Tomadores de decisão em TI (CIO/gestores/FinOps)**: comparar custo/desempenho, simular cenários e justificar decisões.
- **Engenharia/DevOps**: granularidade por região/tipo de instância e rastreabilidade das fontes.
- **Sustentabilidade/ESG**: PUE, % renováveis, metas e evidências por provedor/região.
- **Acadêmicos/pesquisadores**: transparência, reprodutibilidade e exportação de dados.

### 3) Aspectos éticos
- **Transparência e reprodutibilidade**: evidenciar o que vem de API oficial vs. scraping; timestamp e link da fonte; declarar limitações.
- **Consentimento & privacidade**: para telemetria do dashboard (cliques/filtros), informar objetivo, anonimizar e oferecer opt-out.
- **Conformidade de scraping**: respeitar termos de uso/robots.txt; priorizar APIs públicas documentadas.
- **Integridade informacional**: sinalizar incertezas/margens de erro; evitar “dark patterns” na UI.
- **Responsabilidade ambiental**: contextualizar PUE/% renováveis por região/época e evitar greenwashing por escolhas gráficas.

### 4) Requisitos de IHC (principais)
- **Usabilidade**: fluxo simples, busca, filtros persistentes e estados vazios explicativos.
- **Acessibilidade**: textos alternativos nos gráficos.
- **Desempenho & feedback**: mensagens de erro claras.
- **Responsividade**: design responsivo.
- **Consistência visual**: cards KPI; gráficos de barra/linha/pizza e relatório interativo (APEX).

---

## Ferramentas de Coleta de Dados (3 técnicas)

### A) Questionário online (survey)
**Objetivo:** priorizar KPIs e tarefas por perfil (TI, FinOps, ESG).

**Como aplicar (protocolo):**
1. Divulgar para públicos-alvo (lista institucional/LinkedIn/contatos).
2. Exibir termo de consentimento; garantir anonimato e finalidade acadêmica.
3. Coletar por 1–2 semanas; amostra mínima por estrato (≥15 por perfil).
4. Analisar frequências e cruzamentos por perfil/experiência.

**Instrumento (modelo de formulário):**
- **Perfil:** cargo; experiência em cloud (0–1 / 2–3 / 4+ anos); provedor principal.
- **Tarefas (Likert 1–5):** comparar custo x região; ver % renováveis; exportar CSV; conferir fonte/data da coleta.
- **KPIs (ranqueamento):** custo/h VM; egress; PUE; % renováveis; SLA; latência.
- **Preferências de UI:** tipo de gráfico; necessidade de *drill-down*; dark mode.
- **Abertas:** “O que mais te impede de decidir rápido hoje?”; “Quais dados faltam?”.

---

### B) Entrevista semiestruturada
**Objetivo:** compreender cenários de decisão (capex→opex, multi-região, metas ESG) e requisitos de confiança.

**Como aplicar:**
1. Amostra teórica: 6–12 participantes (mix TI/FinOps/ESG).
2. Sessões remotas de 30–45 min; gravação mediante consentimento.
3. Roteiro fixo + *probes*; transcrição e análise temática.

**Instrumento:**
- Contexto atual de uso de cloud.
- Como compara provedores hoje? Quais dados fecham a decisão?
- Indicadores ambientais importam? Como são reportados?
- O que precisa ver na tela para confiar? (fontes, datas, fórmulas)

---

### C) Teste de usabilidade com tarefas 
**Objetivo:** medir eficácia/eficiência/satisfação ao usar o dashboard.

**Como aplicar (protocolo):**
1. Prototipar telas no APEX (ou Figma) com dados fictícios coerentes.
2. 5–8 participantes por rodada/por perfil; 20–30 min por sessão.
3. Coletar taxa de sucesso, tempo por tarefa, erros e SUS (System Usability Scale).
4. Iterar (testar → corrigir → retestar).

**Instrumento (roteiro de tarefas + planilha de registro):**
- **T1:** comparar custo/h de VM entre 2 provedores na região X e exportar CSV.
- **T2:** encontrar a região com melhor PUE e % renováveis para o serviço Y.
- **T3:** localizar “fonte do dado” e timestamp da coleta.
- **T4:** aplicar múltiplos filtros e salvar/compartilhar a visão.
- **Pós-tarefa:** SUS + pergunta aberta (“O que te confundiu?”).
