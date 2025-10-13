# Coleta de Dados

## 1. Identificação de Necessidades dos Usuários e Requisitos de IHC

### Que dados coletar?

#### **Dados do Usuário**
- **Dados demográficos e profissionais:**  
  Cargo atual (Engenheiro de Segurança, Operador de Drone, Supervisor de Obra, Técnico de Segurança), tempo de experiência na função e na área da construção civil, além da formação acadêmica (Engenharia Civil, Segurança do Trabalho, Técnico em Edificações, etc.).

- **Idiomas e jargões técnicos:**  
  Levantar a terminologia usada pelos profissionais para se referir a locais do canteiro (“base”, “fundação”, “frente de obra”), equipamentos (“retroescavadeira”, “guindaste”, “betoneira”) e comportamentos (“afastamento de risco”, “zona segura”).

#### **Dados sobre a relação com a tecnologia**
- **Alfabetismo digital:**  
  Avaliar o grau de familiaridade com drones, câmeras, tablets e softwares de monitoramento.
  
- **Experiência com ferramentas semelhantes:**  
  Verificar se já utilizam tecnologias de segurança ou visão computacional (por exemplo, câmeras fixas de CFTV ou aplicativos de auditoria de segurança).  
  Identificar as dificuldades atuais (limitação de bateria, baixa visibilidade, excesso de alertas).

- **Tecnologia disponível:**  
  Mapear os dispositivos usados na obra (tipo de drone, computador, rede Wi-Fi, sistema de vídeo).

#### **Dados sobre o conhecimento do domínio**
- Nível de conhecimento sobre normas de segurança (NR-18, NR-35) e protocolos de prevenção de acidentes.
- Entendimento sobre análise de risco e monitoramento de atividades em canteiros.

#### **Dados sobre as tarefas**
- **Objetivos e frequência:**  
  Identificar o propósito principal ao usar o sistema (detectar riscos, registrar atividades, gerar relatórios, acompanhar trabalhadores).  
  Definir a frequência de uso (tempo real, diário, semanal).

- **Dores e dificuldades atuais:**  
  Investigar problemas enfrentados hoje, como a falta de histórico de imagens, ângulos cegos das câmeras ou demora na identificação de comportamentos de risco.

- **Gravidade dos erros:**  
  Entender o impacto de falhas do sistema, como não detectar um trabalhador próximo a uma escavadeira ou uma movimentação perigosa.

#### **Dados sobre motivações e valores**
- **Atitudes:**  
  Avaliar a abertura dos profissionais à adoção de novas tecnologias no ambiente de trabalho.

- **Valor percebido:**  
  Identificar o que é mais valorizado: precisão, velocidade, facilidade de uso, confiabilidade ou visualização intuitiva.

---

### De quem coletar?

Os dados serão coletados de **usuários diretos e stakeholders secundários**.

| Persona | Perfil | Foco da Coleta |
|----------|---------|----------------|
| **Operador de Drone** | Responsável pela captura das imagens e operação do drone. | Limitações de voo, interferências, tempo de operação e controle de qualidade das imagens. |
| **Engenheiro de Segurança** | Analisa riscos e elabora relatórios de segurança. | Necessidades de alertas, visualização de eventos e histórico de detecções. |
| **Supervisor de Obra** | Garante o cumprimento das normas de segurança em campo. | Preferências sobre notificações e acompanhamento de incidentes em tempo real. |

**Stakeholders secundários:**
- Diretoria da construtora (interessada em indicadores de segurança e produtividade).  
- Equipe de TI (suporte técnico e integração com sistemas internos).

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

## 3. Ferramentas de Coleta de Dados

### 3.1 **Instrumento 2: Questionário de Perfil e Expectativas do Usuário**

**Objetivo:**  
Coletar dados quantitativos sobre o perfil profissional, o nível de familiaridade tecnológica e o grau de aceitação das soluções de monitoramento baseadas em drones e inteligência artificial.

---

**Como aplicar:**  

**Criação da Ferramenta:**  
O questionário será implementado na plataforma Google Forms, por ser de fácil acesso e permitir a exportação dos dados para análise posterior. O formulário será estruturado em quatro seções principais, com perguntas de múltipla escolha e escalas de Likert (1 a 5):  
1. Perfil profissional e tempo de experiência.  
2. Nível de familiaridade com tecnologia.  
3. Dificuldades e expectativas em relação ao uso de drones e IA.  
4. Importância das funcionalidades do sistema (alertas, relatórios, histórico visual).  

**Teste Piloto:**  
Antes de disponibilizar o questionário aos profissionais do canteiro, será realizado um teste piloto com 2 ou 3 integrantes da equipe de desenvolvimento. O objetivo é garantir clareza nas perguntas, ausência de erros e tempo de preenchimento adequado (idealmente entre 10 e 15 minutos).

**Recrutamento e Contato:**  
O contato com os profissionais será feito por meio do engenheiro responsável pela obra ou do supervisor de campo, que distribuirá o link do formulário aos colaboradores que se enquadrem nos perfis de interesse (operadores de drone, engenheiros de segurança e supervisores de obra).

**Aplicação:**  
O formulário será disponibilizado por meio de um link compartilhado via e-mail ou aplicativo de mensagens corporativo. A mensagem de convite incluirá:  
- O objetivo do formulário e sua relevância para o aprimoramento da segurança e do monitoramento no canteiro.  
- O tempo estimado para resposta.  
- Um aviso de que as respostas serão tratadas de forma confidencial e utilizadas apenas para aprimorar o sistema.  
- O link direto para o questionário.  

**Coleta e Análise:**  
O formulário ficará disponível por um período determinado (por exemplo, até 10 dias). Após o encerramento da coleta, os dados serão exportados e segmentados por perfil de usuário, permitindo uma análise comparativa entre grupos profissionais (operacional, técnico e gerencial).


**Instrumento:**
[Formulário Google Forms](https://docs.google.com/forms/d/e/1FAIpQLSdVRtycJva3RF0Ij9XHeC9BpVIAIQBwDdmFXlrnv_STzXIEOA/viewform?usp=header)

---
