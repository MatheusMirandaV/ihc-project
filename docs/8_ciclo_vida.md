**CICLO DE VIDA DE ENGENHARIA DE USABILIDADE**

![Ciclo de vida](imagens/ciclo_de_vida.png)

1. **Características da Plataforma**  
   

| Característica | Descrição |
| :---- | :---- |
| Descrição do Software | A aplicação foi desenvolvida na plataforma Oracle APEX, hospedada em um Oracle Autonomous Transaction Processing (ATP), versão Always Free. O sistema utiliza SQL e PL/SQL para manipulação e agregação dos dados, além de componentes nativos de interface do APEX (gráficos, cartões e relatórios interativos) para visualização. O design segue o tema Oracle Redwood, garantindo acessibilidade e consistência visual |
| Descrição do Hardware | A aplicação é executada em ambiente em nuvem Oracle Cloud Infrastructure (OCI). O banco de dados está alocado em uma instância de ATP com 1 OCPU compartilhado e 20 GB de armazenamento. O acesso do usuário ocorre via navegador web, sem necessidade de instalação local. A coleta de dados é feita por scripts Python executados em máquinas locais ou instâncias de computação da nuvem, conforme o ciclo de coleta |
| LISTA DE Capacidades da Plataforma (com explicação) | Escalabilidade: a infraestrutura em nuvem permite aumento de recursos conforme a demanda de dados cresce.• Disponibilidade: o Oracle APEX garante alta disponibilidade (SLA ≥ 99.95%) e suporte multiusuário.• Segurança: o banco de dados ATP aplica criptografia transparente (TDE), autenticação gerenciada e isolamento de dados.• Integração com APIs: capacidade de importar dados externos por REST APIs dos provedores (AWS, GCP, OCI).• Visualização Interativa: gráficos e painéis dinâmicos, com filtros e drill-down, suportados nativamente pelo APEX.• Acessibilidade: compatibilidade com padrões WCAG e uso do tema Redwood para contraste e legibilidade |
| LISTA DE Restrições da Plataforma (com explicação) | Limite de Recursos (Free Tier): a instância ATP gratuita possui restrições de CPU e armazenamento, o que pode impactar a performance em consultas complexas.• Dependência de Conexão Internet: por ser uma aplicação 100% web, o uso offline não é possível.• Limitação de Customização no Front-end: o APEX impõe restrições a personalizações visuais avançadas fora do tema Redwood.• Tempo de Sessão: o APEX encerra sessões inativas automaticamente após determinado tempo (configuração padrão de 30 minutos).• Diferença de Formatos Regionais: campos de data e número dependem das configurações de localidade, o que exige padronização (por exemplo, formato DD-MM-YYYY). |

2. **Princípios Gerais do Projeto (INCREMENTAR TABELA)**     

| Nome | Descrição | Link |
| :---- | :---- | :---- |
| Descrição do Contexto | O projeto tem como objetivo avaliar o impacto da migração para a nuvem na eficiência operacional e na inovação tecnológica, por meio de um sistema de análise e visualização de dados desenvolvido no Oracle APEX. O foco é garantir que a ferramenta seja segura, acessível e centrada no usuário, respeitando princípios éticos e legais.  |  |
| Lei Geral de Proteção de Dados (LGPD) \- Lei n.º 13.709/2018 | A LGPD é a legislação brasileira que regulamenta o tratamento de dados pessoais no Brasil. É importante para o projeto porque estabelece regras sobre como os dados dos usuários devem ser coletados, armazenados, processados e protegidos, garantindo sua privacidade e segurança. | [https://www.planalto.gov.br/ccivil\_03/\_ato2015-2018/2018/lei/l13709.htm](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) |
| Lei n.º 10.098/2000 \- Lei da Acessibilidade |  Esta lei brasileira estabelece normas gerais e critérios básicos para a promoção da acessibilidade das pessoas com deficiência ou com mobilidade reduzida. É importante para o projeto porque define diretrizes para tornar produtos e serviços, incluindo interfaces de usuário, acessíveis a todos os usuários, independentemente de suas habilidades físicas ou cognitivas. | [https://www.planalto.gov.br/ccivil\_03/leis/l10098.htm](https://www.planalto.gov.br/ccivil_03/leis/l10098.htm) |
| ABNT NBR ISO 9241 Ergonomia da interação humano-sistema |  Esta série de normas brasileiras, baseadas nas normas ISO 9241, fornece diretrizes e orientações para o design centrado no usuário de sistemas interativos, incluindo a concepção de interfaces de usuário. A parte 210 aborda o processo de design centrado no humano, enquanto a parte 11 fornece orientações específicas sobre usabilidade. Essas normas são importantes para o projeto porque estabelecem princípios e métodos para garantir que a interface do usuário atenda às necessidades e expectativas dos usuários. | [https://www.inf.ufsc.br/\~edla.ramos/ine5624/\_Walter/Normas/Parte%2011/iso9241-11F2.pdf](https://www.inf.ufsc.br/~edla.ramos/ine5624/_Walter/Normas/Parte%2011/iso9241-11F2.pdf) |
|  | . |  |

   

3. **Metas de Usabilidade**

   1. **Qualitativo**

    


   2. **Quantitativo**  
    
| Metas | Porcentagem | Justificativa |
| ----- | :---- | :---- |
| Facilidade de … | 20% | O sistema deve ser intuitivo e permitir que novos usuários compreendam suas funcionalidades (filtros, gráficos, relatórios) sem treinamento formal. |
|Satisfação do usuário  | 15% | O dashboard deve transmitir clareza, confiança e estética agradável, refletindo profissionalismo e confiabilidade nos resultados apresentados. |
|Consistência visual e navegação  | 10% | A aplicação deve manter um padrão visual coerente (tema Oracle Redwood), facilitando a navegação e reduzindo a carga cognitiva. |
| Eficiência de uso | 20% | O usuário deve conseguir gerar e interpretar um relatório completo em menos de 2 minutos. |
| Taxa de erro de interação | 10% | Menos de 5% das interações devem resultar em erros  |
| Compreensão das métricas | 10% |  Pelo menos 80% dos usuários devem interpretar corretamente os indicadores apresentados (como custo médio, PUE e intensidade de carbono).|
| Tempo de resposta do sistema | 15% | As páginas devem carregar em até 3 segundos, mesmo com múltiplos filtros ativos. |
| **Total** | **100%** |  |
