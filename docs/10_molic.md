## MOLIC

Agentes
- **Usuário**: pessoa que navega, filtra e interpreta as visualizações do dashboard.
- **Sistema**: aplicação Oracle APEX que processa filtros, carrega dados e atualiza gráficos.

Variáveis de Estado
- **Filtros selecionados** (provedor, país, região, métrica, período).
- **Dados carregados** (métricas normalizadas, KPIs calculados).
- **Modo de visualização** (gráficos, tabelas comparativas, drill-down).
- **Feedback da interface** (loading, tooltip, mudança de gráfico, destaque visual).

Ações Principais

| Ação do Usuário | Resposta do Sistema | Variáveis Alteradas |
|------------------|----------------------|----------------------|
| Selecionar provedor | Atualiza gráficos e KPIs filtrados | filtros, dados carregados |
| Selecionar período | Recalcula métricas exibidas | filtros, dados carregados |
| Selecionar métrica (custo, PUE, CO₂ etc.) | Atualiza visualização correspondente | modo de visualização |
| Clicar em um provedor/gráfico | Exibe detalhamento (drill-down) | modo de visualização |
| Remover filtros | Restaura visão geral | filtros, dados carregados |
| Passar o mouse sobre gráficos | Exibe tooltip com valores | feedback da interface |

Diagrama MOLIC 

<img src="/docs/imagens/molic.png" width="700">
