# Análise de Tarefas

A equipe deve descrever as funcionalidades mais importantes da interface.  
São apresentados a seguir:  
- 1 HTA  
- 1 GOMS  
- 1 CTT envolvendo ao menos 4 funcionalidades

---

## 1. HTA – Hierarchical Task Analysis  
### Funcionalidade: Comparar custo médio entre dois provedores de nuvem

**Descrição**  
O usuário deseja comparar o custo médio entre dois provedores (ex.: AWS x OCI). A tarefa envolve selecionar provedores, definir período e interpretar o gráfico.

**HTA (descrição hierárquica)**  
**0. Comparar custo médio entre dois provedores**  
&nbsp;&nbsp;0.1 Acessar painel “Custo / Eficiência”  
&nbsp;&nbsp;0.2 Selecionar Provedor A  
&nbsp;&nbsp;0.3 Selecionar Provedor B  
&nbsp;&nbsp;0.4 Definir período  
&nbsp;&nbsp;0.5 Aplicar filtros  
&nbsp;&nbsp;0.6 Analisar gráfico  
&nbsp;&nbsp;0.7 Interpretar resumo  
&nbsp;&nbsp;0.8 Ajustar filtros (opcional)

**Decomposição detalhada**  
- **0.1 Acessar painel**  
  - 0.1.1 Abrir aplicação  
  - 0.1.2 Abrir menu lateral  
  - 0.1.3 Selecionar “Custo / Eficiência”

- **0.2 Selecionar Provedor A**  
  - 0.2.1 Abrir dropdown  
  - 0.2.2 Escolher provedor desejado  

- **0.3 Selecionar Provedor B**  
  - 0.3.1 Abrir dropdown  
  - 0.3.2 Escolher provedor desejado  

- **0.4 Definir período**  
  - 0.4.1 Abrir seletor de data  
  - 0.4.2 Selecionar data inicial  
  - 0.4.3 Selecionar data final  

- **0.5 Aplicar filtros**  
  - 0.5.1 Clicar em “Aplicar filtros”  
  - 0.5.2 Aguardar atualização  

- **0.6 Analisar gráfico**  
  - 0.6.1 Observar barras/linhas  
  - 0.6.2 Comparar valores  

- **0.7 Interpretar resumo**  
  - 0.7.1 Ler texto de destaque  

## 2. GOMS  
### Funcionalidade: Verificar emissões de carbono (CO₂e) de um provedor em uma região

### Goals  
- **G1:** Ver emissões de CO₂e por região  
- **G2:** Opcional — comparar outra região

### Operators  
O1: Mover cursor  
O2: Clicar em menu  
O3: Abrir dropdown provedor  
O4: Selecionar provedor  
O5: Abrir filtro de região  
O6: Selecionar região  
O7: Abrir seletor de métricas  
O8: Selecionar “CO₂e”  
O9: Aplicar filtros  
O10: Aguardar atualização  
O11: Passar mouse sobre gráfico  
O12: Ler valor do tooltip

### Methods  
**M1 — Para alcançar G1**  
1. O1  
2. O2 – Abrir painel de sustentabilidade  
3. O3  
4. O4  
5. O5  
6. O6  
7. O7  
8. O8  
9. O9  
10. O10  
11. O11  
12. O12

**M2 — Para alcançar G2**  
1. Repetir passos 5-12 do M1 mudando apenas a região.

### Selection Rules  
- **SR1:** Se já estiver no painel certo, iniciar no passo 3.  
- **SR2:** Se quiser análise geral, pular passo 5-6.

## 3. CTT – ConcurTaskTrees  
### Funcionalidades modeladas
1. Explorar visão geral do painel  
2. Ajustar período  
3. Selecionar métrica (custo, desempenho, ambiental)  
4. Acessar detalhamento (drill-down)
