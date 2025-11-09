# Coleta de Dados

## 1. Identificação de Necessidades dos Usuários e Requisitos de IHC

### Dados a Coletar

#### Dados do Usuário
- **Demográficos e profissionais:** Cargo na empresa (pesquisador, engenheiro de IA, analista de dados), experiência em desenvolvimento de modelos, área de especialização (visão computacional, aprendizado de máquina, etc.).  
- **Idiomas e jargões técnicos:** Termos usados para se referir a modelos de IA, métricas de performance (accuracy, precision, recall, F1-score), tipos de datasets e formatos de vídeo/imagem.

#### Relação com a tecnologia
- **Alfabetismo digital:** Familiaridade com interfaces de teste de modelos, notebooks, softwares de análise de dados e dashboards.  
- **Experiência prévia:** Uso de ferramentas de teste de modelos, validação de IA ou monitoramento em tempo real.  
- **Tecnologia disponível:** Computadores, GPUs, ambientes de teste em cloud/local, câmeras ou datasets simulados.

#### Conhecimento do domínio
- Experiência em monitoramento de segurança, análise de risco ou operações em canteiros de obras (caso necessário para interpretar os resultados).  
- Familiaridade com métricas de avaliação de IA e análise de desempenho de modelos.

#### Tarefas e objetivos
- Finalidade do uso do sistema: testar diferentes modelos de IA, comparar resultados, gerar relatórios de métricas e definir o melhor modelo a ser utilizado.  
- Frequência de uso: diário ou durante ciclos de desenvolvimento/teste.  
- Dores e dificuldades: dificuldade em interpretar métricas complexas, necessidade de comparar rapidamente múltiplos modelos, falta de histórico organizado de execuções.  
- Gravidade dos erros: impacto de selecionar um modelo inadequado para produção.

#### Motivações e valores
- Abertura para novas interfaces que agilizem testes e análises.  
- Valor percebido em clareza visual, velocidade de execução, confiabilidade do sistema e facilidade de exportação de resultados.

---

### De quem coletar

| Persona | Perfil | Foco da Coleta |
|---------|--------|----------------|
| Empresa desenvolvedora do modelo | Profissionais responsáveis por testar modelos | Facilidade de uso, comparação de modelos, geração de relatórios |
| Pesquisadores / Equipe de validação | Usuários que analisam resultados e métricas | Visualização de métricas, interpretação de resultados, integração com dados de teste |

**Stakeholders secundários:**  
- Gerentes de projeto (interessados na eficiência e confiabilidade dos testes).  
- Equipe de TI/DevOps (responsável pelo ambiente de execução, manutenção e armazenamento de dados).

---

## 2. Aspectos Éticos

A coleta de dados deve respeitar os princípios éticos fundamentais, considerando que envolve pessoas e imagens em ambiente profissional.

### **Princípio da Autonomia**
- Todos os participantes deverão assinar um **Termo de Consentimento Livre e Esclarecido (TCLE)**.  
- Eles serão informados sobre os objetivos acadêmicos do projeto, o uso dos dados (para treinamento e validação da IA) e o direito de desistir a qualquer momento sem prejuízo.

### **Princípio da Não Maleficência e Beneficência**
- As informações coletadas **não serão usadas para avaliações de desempenho** dos trabalhadores.  
- O objetivo é **melhorar a segurança e prevenir acidentes**, garantindo o bem-estar dos colaboradores.  
- As entrevistas e observações devem causar o mínimo de desconforto possível.

### **Privacidade e Confidencialidade**
- As imagens e dados coletados serão **anonimizados**, evitando identificação facial ou nominal.  
- O armazenamento será feito em ambiente seguro, com acesso restrito à equipe de pesquisa.  
- Em relatórios e apresentações, as informações serão apresentadas de forma **agregada e sem identificação individual**.

### **Princípio da Justiça e Equidade**
- Os resultados do projeto devem trazer **benefícios diretos aos trabalhadores**, como um ambiente mais seguro.  
- O tempo dedicado pelos participantes deve ser reduzido e respeitado.  
- A participação será totalmente **voluntária**.

---


## 3. Ferramentas de Coleta de Dados (três técnicas diferentes)

### 3.1 Nome do instrumento: Questionário de Perfil de Usuário e Priorização de Funcionalidades

* **Objetivo da aplicação:**
  * **Validar o Perfil:** Coletar dados técnicos e profissionais para confirmar e quantificar as características dos usuários que testam modelos de IA (engenheiros de machine learning, analistas de dados, gestores de tecnologia).
  * **Mapear Dores Atuais:** Entender as principais dificuldades enfrentadas pelas equipes no processo de teste, comparação e análise de modelos de IA.
  * **Priorizar Funcionalidades:** Medir o grau de importância que cada perfil atribui às funcionalidades propostas para a interface, como upload de modelos, visualização de métricas, comparação de resultados e exportação de relatórios.

* **Explicar como aplicar:**
  * **Criação da Ferramenta:** O questionário será implementado na plataforma **Google Forms**, por ser de fácil acesso e permitir exportação dos dados para análise quantitativa.
  * **Teste Piloto:** Antes do envio oficial, o questionário será testado com 2 ou 3 integrantes da equipe do projeto para verificar clareza das perguntas, possíveis redundâncias e tempo de preenchimento (estimado entre 10–15 minutos).
  * **Recrutamento e Contato:** O convite será enviado a profissionais da empresa parceira que atuam diretamente com o desenvolvimento e validação de modelos. O contato poderá ser feito via e-mail institucional ou grupo interno de comunicação.
  * **Aplicação:** O e-mail de convite conterá:
    * Uma breve explicação sobre o objetivo do projeto e da pesquisa.  
    * O tempo estimado de resposta.  
    * O **Termo de Consentimento**, garantindo anonimato, confidencialidade e uso dos dados apenas para fins acadêmicos.  
    * O link para o questionário.  
  * **Coleta e Análise:** O questionário ficará aberto por um período de 10 dias. Após o encerramento, os dados serão exportados e segmentados por perfil (desenvolvedor, analista e gestor) para análise comparativa.

* **Instrumento:** [Formulário Google Forms](https://docs.google.com/forms/d/e/1FAIpQLSdVRtycJva3RF0Ij9XHeC9BpVIAIQBwDdmFXlrnv_STzXIEOA/viewform?usp=header)

---

### 3.2 Nome do instrumento: Observação Simples

* **Objetivo da aplicação:**
  * Entender o fluxo real de trabalho dos profissionais durante o teste de modelos de IA.  
  * Identificar gargalos, comportamentos recorrentes e problemas de usabilidade nas ferramentas atuais.  
  * Coletar dados contextuais sobre o ambiente de trabalho e as condições em que o sistema é utilizado (hardware, datasets, tempo de execução, interação entre equipes).

* **Explicar como aplicar:**
  * Solicitar autorização formal para acompanhar as atividades, garantindo que a observação não interfira na rotina e que não se trata de avaliação de desempenho.  
  * O observador permanecerá próximo ao usuário durante o uso da interface (ou ferramenta atual), observando silenciosamente.  
  * As anotações serão feitas em um **roteiro estruturado**, registrando comportamentos, expressões e dificuldades encontradas.  

* **Instrumento: Roteiro/Checklist de Observação**
  * **Participantes:**  
    * 1 ou 2 desenvolvedores de IA (Ricardo Santos – Gerente de Segurança).  
    * 1 ou 2 analistas de validação de modelos (Fernanda Costa – Engenheira e Gestora de Obra).  
    * 1 técnico de apoio em teste e execução (João – Técnico de Segurança).  

  * **Para o Gerente de Segurança (Ricardo):**
    * [ ] Quais métricas ele verifica com mais frequência nos relatórios?  
    * [ ] Ele compreende facilmente as visualizações de desempenho?  
    * [ ] Há dificuldades em interpretar comparações entre modelos?  
    * [ ] Em quais momentos ele solicita apoio da equipe técnica?  
    * [ ] Ele sugere novas formas de exibir resultados (ex.: dashboards mais visuais)?  

  * **Para a Engenheira e Gestora (Fernanda):**
    * [ ] Quais passos ela realiza para carregar e executar os modelos?  
    * [ ] Quanto tempo leva para obter os resultados após o upload?  
    * [ ] Há momentos de espera, dúvida ou repetição de ações?  
    * [ ] Ela utiliza anotações externas (planilhas, cadernos)?  
    * [ ] Há alguma dificuldade em entender as métricas apresentadas?  

  * **Para o Técnico de Segurança (João):**
    * [ ] Ele consegue iniciar o teste sem ajuda externa?  
    * [ ] Compreende os alertas ou erros gerados pela interface?  
    * [ ] Qual é a ação mais repetitiva que ele realiza?  
    * [ ] Ele demonstra frustração ou hesitação durante o processo?  
    * [ ] Há interferências do ambiente físico (luz, ruído, distrações)?  

---

### 3.3 Nome do instrumento: Sessão de Brainstorming

* **Objetivo da aplicação:**
  * Gerar uma lista de funcionalidades desejadas para a interface de testes de modelos.  
  * Compreender prioridades e expectativas dos diferentes perfis de usuário.  
  * Promover a colaboração entre técnicos e gestores para co-criação de melhorias.

* **Explicar como aplicar:**
  * Reunir os participantes em uma sala de reunião ou espaço digital com quadro interativo (ex.: Miro ou Mural).  
  * O moderador explica o objetivo da sessão e estabelece as regras: “Nenhuma ideia é ruim — o foco é gerar o máximo possível de sugestões.”  
  * Utilizar um roteiro estruturado para guiar o processo.

* **Instrumento: Roteiro/Agenda do Brainstorming**
  * **Participantes:** Um grupo de 4 a 6 pessoas, incluindo:
    * Ricardo Santos (Gerente de Segurança);  
    * Fernanda Costa (Engenheira e Gestora de Obra);  
    * João (Técnico de Segurança);  
    * 1 integrante da equipe de desenvolvimento da interface.  

  1. **Introdução e Apresentação do Problema (5 minutos)**  
     * “Estamos desenvolvendo uma interface para que as empresas possam testar e comparar modelos de IA de monitoramento em tempo real. Atualmente, o processo é fragmentado, pouco intuitivo e dificulta a análise de métricas. Nosso objetivo é entender como podemos tornar essa experiência mais eficiente e visual.”  

  2. **Geração de Ideias Individuais (10 minutos)**  
     * “Se você pudesse criar a ferramenta perfeita para o seu trabalho, o que ela faria? Pense em tudo — automação, comparação, alertas, relatórios, visualização 3D, etc.”  
     * “Escreva cada ideia em um post-it (ou nota virtual) separado.”  

  3. **Compartilhamento e Agrupamento (20 minutos)**  
     * Cada participante apresenta suas ideias, e o moderador agrupa em temas, como:  
       * Relatórios Automáticos  
       * Comparação de Modelos  
       * Interface Visual Intuitiva  
       * Alertas Inteligentes  
       * Exportação e Compartilhamento  

  4. **Votação e Priorização (5 minutos)**  
     * Cada participante recebe 3 votos (adesivos virtuais) para escolher as ideias mais relevantes.  
     * As ideias mais votadas serão consideradas prioritárias para o próximo protótipo da interface.  

  5. **Encerramento (5 minutos)**  
     * “Com isso, temos uma visão clara das funcionalidades mais importantes para o sistema. Suas contribuições são essenciais para desenvolvermos uma interface realmente útil e eficiente.”  
     * Agradecimento e registro das ideias no mural digital.  

---
