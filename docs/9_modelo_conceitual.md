1) **Cenários de Interação**
> **_NOTE:_**: destacar em negrito o texto alterado entre Cenário Problema e Cenário de Interação

2) **Design Centrado na Comunicação**

**Nome do Cenário: Consulta e comparação de emissões de carbono entre provedores de nuvem


| tópico \> subtópico (diálogo) | falas e signos |
| :---- | :---- |
| O usuário acessa o painel “Impacto Ambiental” no dashboard. Signos: Ícone de nuvem - menu lateral “Sustentabilidade” e observar grafico | U: U: Preciso avaliar qual provedor tem menor emissão de carbono |
| O usuário seleciona o filtro “Métrica: Intensidade de Emissão e define o período “Últimos 3 meses”.| U: Quero visualizar as emissões médias por kWh. |
| O sistema exibe um gráfico de barras com cores distintas para cada provedor. Signos: Barras coloridas, eixo Y = “kgCO₂/kWh”, tooltip dinâmico com valores| D: Aqui está o gráfico comparativo.  |
| O usuário clica na barra correspondente à Google Cloud.| U: Quero detalhar apenas a Google Cloud  |
|O sistema aplica o filtro automático e exibe: Tabela detalhada com variação mensal das emissões; |D: Aqui está a informação filtrada |

3) **Mapa de Objetivos**

O sistema foi projetado para analisar e visualizar dados sobre a migração para a nuvem, com foco em eficiência operacional, custo e sustentabilidade ambiental.
 O mapa de objetivos representa a relação entre as necessidades dos usuários (analistas e pesquisadores), os objetivos funcionais e não funcionais do sistema e os critérios de usabilidade que sustentam a experiência de uso.

Objetivos do Usuário

U1. Comparar provedores de nuvem com base em custo, desempenho e impacto ambiental.

U2. Obter relatórios visuais e interpretáveis sem precisar de conhecimento técnico avançado.

U3. Acessar informações de forma rápida, intuitiva e visualmente clara.

U4. Garantir que os dados apresentados sejam confiáveis e rastreáveis.


Objetivos do Sistema

S1. Coletar e consolidar dados de múltiplos provedores (AWS, GCP, Oracle Cloud).

S2. Normalizar e armazenar métricas em um banco Oracle ATP.

S3. Exibir dashboards interativos no Oracle APEX com filtros e comparativos.

S4. Garantir acessibilidade, segurança e integridade dos dados exibidos.


Critérios de Usabilidade

C1. Facilidade de aprendizado

C2. Eficiência de uso.

C3. Satisfação visual e estética (uso do tema Oracle Redwood).

C4. Redução de erros e respostas rápidas (tempo de carregamento ≤ 3s).

C5. Acessibilidade e compatibilidade com dispositivos e leitores de tela.

     ligações
    U1 --> S1
    U1 --> S2
    U1 --> S3
    U2 --> S3
    U3 --> S3
    U3 --> C1
    U3 --> C2
    U3 --> C3
    U4 --> S4
    S1 --> C2
    S2 --> C4
    S3 --> C1
    S3 --> C3
    S4 --> C5


4) **Esquema Conceitual de Signos**

> **_NOTE:_**: fazer a junção das 3 tabelas abaixo em uma única

| Credenciais (C) \- credenciais para acesso ao sistema |  |  |
| :---- | :---- | :---- |
| **signo** | **origem** | **observações** |
| usuário | domínio |  |
| senha | domínio |  |

| Credenciais (C) \- credenciais para acesso ao sistema |  |  |  |
| :---- | :---- | :---- | :---- |
| **signo** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** |
| usuário | texto | não pode ser nulo | — |
| senha | texto | não pode ser nulo | — |

| Credenciais (C) \- credenciais para acesso ao sistema |  |  |
| :---- | :---- | :---- |
| **signo** | **prevenção** | **recuperação** |
| usuário | PP: campo obrigatório | RA |
| senha | PP campo obrigatório  | RA |
