# Personas e Contexto de Uso

---

# Personas

- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais características e contextos sociais, econômicos e culturais.

---

## Persona Primária

### Engenheiro de Machine Learning
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/e5e2cc25-8642-428a-83e1-b06eea16e193" />

**Identidade:**
- Nome: Paulo Andrade  
- Idade: 30 anos  
- Formação: Engenheiro da Computação  
- Experiência: 5 anos com visão computacional e aprendizado profundo

**Status:** Persona Primária

**Objetivos:**
- Pessoais: Ser referência em IA aplicada à segurança do trabalho.  
- Práticos:
  - Subir, testar e comparar diferentes modelos de IA em um ambiente padronizado.
  - Avaliar desempenho com dados reais e sintéticos.
  - Automatizar geração de métricas (precisão, recall, F1-score).

**Habilidades:**
- Domínio de frameworks (TensorFlow, PyTorch).
- Experiência com manipulação de imagens e vídeo.
- Habilidade intermediária com dashboards e ferramentas de validação.

**Tarefas:**
- Críticas: Treinar, subir e validar modelos; interpretar métricas; gerar relatórios.
- Frequência: Testes diários durante as fases de desenvolvimento.
- Duração: Ciclos contínuos (semanas a meses).

**Relacionamentos:**
- Trabalha com analistas de dados e desenvolvedores.
- Reporta resultados ao gerente técnico do projeto.
- Interface com clientes corporativos e times de produto.

**Requisitos:**
- Interface para upload e execução rápida de modelos.
- Visualização gráfica e tabular das métricas de inferência.
- Exportação automática de relatórios.

**Expectativas:**
- Comparação direta entre versões de modelos sem scripts.
- Relatórios detalhados e reproduzíveis.
- Redução do tempo gasto em tarefas manuais e repetitivas.

---

## Persona Secundária

### Gerente de Segurança do Trabalho
<img width="400" height="400" alt="{BAD433DE-DBC7-4268-B9CE-7F88D4DD5A5D}" src="https://github.com/user-attachments/assets/712b7f27-e797-496b-8c8b-dfd901095af5" />

**Identidade:**
- Nome: Ricardo Santos  
- Idade: 45 anos  
- Formação: Engenheiro de Segurança do Trabalho  
- Experiência: 18 anos em gestão de segurança ocupacional

**Status:** Persona Secundária

**Objetivos:**
- Pessoais: Modernizar processos de segurança e reduzir acidentes.
- Práticos:
  - Avaliar confiabilidade dos modelos antes da implantação.
  - Compreender relatórios técnicos em linguagem acessível.
  - Garantir que o modelo detecte situações de risco relevantes.

**Habilidades:**
- Conhecimento profundo das NRs e requisitos de conformidade.
- Familiaridade com dashboards corporativos.

**Tarefas:**
- Críticas: Revisar e aprovar modelos para uso em campo.
- Frequência: Semanal/quinzenal, conforme ciclos de entrega.
- Duração: Supervisão durante o desenvolvimento e fases piloto.

**Relacionamentos:**
- Coordena técnicos de segurança e interage com times de IA.
- Reporta à diretoria sobre riscos e decisões de implantação.

**Requisitos:**
- Relatórios visuais e indicadores de desempenho voltados à segurança.
- Tradução de métricas técnicas para indicadores de risco.

**Expectativas:**
- Transparência sobre limitações e acertos dos modelos.
- Ferramenta que facilite a validação técnica e a decisão operacional.

---

## Persona Terciária

### Gestora de Projetos de Inovação
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/9e5b3358-7269-4b93-ba0a-6fc589393708" />

**Identidade:**
- Nome: Fernanda Costa  
- Idade: 38 anos  
- Formação: Engenheira Civil com MBA em Gestão de Projetos  
- Experiência: 12 anos em gestão de obras e coordenação de projetos de inovação

**Status:** Persona Terciária

**Objetivos:**
- Pessoais: Liderar transformação digital na empresa.
- Práticos:
  - Acompanhar evolução dos modelos e justificar investimentos.
  - Apresentar resultados técnicos de forma estratégica.
  - Garantir alinhamento entre times técnicos e executivos.

**Habilidades:**
- Gestão de equipes multidisciplinares.
- Comunicação executiva e entendimento estratégico.

**Tarefas:**
- Críticas: Monitorar progresso do projeto e reportar a stakeholders.
- Frequência: Quinzenal em reuniões de acompanhamento.
- Duração: Durante todo o ciclo de desenvolvimento da solução.

**Relacionamentos:**
- Interage com direção, investidores e clientes.
- Coordena entregas entre segurança, IA e produto.

**Requisitos:**
- Relatórios executivos prontos para apresentação.
- Visualizações simples e padronizadas.

**Expectativas:**
- Que a interface simplifique a comunicação entre técnica e gestão.
- Relatórios confiáveis que suportem decisões de investimento.

---

# Informações que o Sistema Deve Armazenar sobre os Usuários

## Dados de Identificação e Acesso:
- Nome completo, cargo, empresa/setor
- Nível de acesso e permissões no sistema (roles)
- Histórico de login e ações (audit trail)
- Certificações e qualificações em segurança / IA

## Dados de Personalização:
- Preferências de interface e alertas
- Dashboards salvos e filtros frequentes

## Dados de Performance e Uso:
- Tempo médio de resposta a testes
- Frequência de uso de funcionalidades (upload, teste, export)
- Efetividade nas análises (ex.: modelos aprovados)
- Feedback sobre usabilidade

## Dados de Contexto Operacional:
- Projetos e obras associadas
- Datasets de teste preferenciais (sintético, real, híbrido)
- Histórico de modelos testados e resultados resumidos

---

# Mapa de Empatia

![Mapa de empatia](imagens/empatia.png)

## Mapa de Empatia — Paulo Andrade (Engenheiro de ML)

**O que ele VÊ?**
- Dashboards com várias métricas e resultados.
- Ferramentas técnicas pouco integradas.
- Pressão por resultados rápidos e reproduzíveis.

**O que ele OUVE?**
- Pedidos por relatórios e justificativas do gerente técnico.
- Feedbacks sobre falhas e necessidade de melhorias.
- Discussões técnicas sobre trade-offs de modelos.

**O que ele PENSA E SENTE?**
- Frustração com processos manuais.
- Vontade de automatizar e padronizar testes.
- Ansiedade quanto à robustez dos modelos em campo.

**O que ele FALA E FAZ?**
- Compara modelos, ajusta hiperparâmetros e valida resultados.
- Gera relatórios e compartilha com gerência.

**DORES**
- Perda de tempo com scripts e coleta manual de métricas.
- Dificuldade em comparar versões de forma confiável.

**GANHOS**
- Relatórios automáticos, comparação visual e economia de tempo.

---

# Contexto de Uso

O sistema será utilizado por **empresas desenvolvedoras de modelos de IA** para **monitoramento de segurança em canteiros de obra**. A plataforma oferece um ambiente unificado para **upload, execução e comparação de modelos**, com suporte a imagens/vídeos reais e sintéticos, e geração automática de relatórios.

**Ambientes de uso:**
- Laboratório de desenvolvimento (engenheiros de ML).
- Sala de gestão (gerentes de segurança e projetos).
- Demonstrações para clientes e pilotos em campo.

**Requisitos de usabilidade:**
- Balancear complexidade técnica e clareza executiva.
- Oferecer workflows guiados para upload e execução de modelos.
- Garantir rastreabilidade e reprodutibilidade dos testes.

---

# Jornada do Usuário

## Engenheiro de Machine Learning — Paulo Andrade

1. Acessa a plataforma web e faz login com seu perfil técnico.  
2. Seleciona ou faz upload de um novo modelo (arquivo / container / endpoint).  
3. Escolhe datasets de testes (vídeos/frames reais e sintéticos) e parâmetros de execução.  
4. Inicia o teste; a plataforma executa inferência e coleta métricas em batch ou streaming.  
5. Visualiza resultados em dashboards (precisão, recall, F1, mAP, tempo de inferência, FPS).  
6. Compara diversos modelos lado a lado; salva configurações e exporta relatórios em PDF/CSV.  
7. Compartilha o relatório com Ricardo (Gerente de Segurança) para validação.

## Gerente de Segurança — Ricardo Santos

1. Recebe notificação de relatório pronto; acessa o dashboard executivo.  
2. Visualiza indicadores traduzidos para métricas de segurança operacional.  
3. Analisa impacto (falsos negativos críticos, taxa de detecção de EPIs, latency).  
4. Aprova ou solicita novos testes com base nos resultados.

## Gestora de Projetos — Fernanda Costa

1. Consulta relatórios consolidados periodicamente.  
2. Usa gráficos e resumos executivos para preparar apresentações.  
3. Decide sobre continuidade do investimento e planejamento de pilotos em campo.

---

