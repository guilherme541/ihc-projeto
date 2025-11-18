# Avaliação de Usabilidade por Observação do Usuário

---

## Fluxograma de Avaliação de Usabilidade por Observação do Usuário

<p align="center">
  <img width="1048" height="145" alt="image" src="https://github.com/user-attachments/assets/0315ae01-8a93-4e46-8569-84b05348f3d0" />
</p>

---

## Descrição do Procedimento de Preparação do Teste

### **Passo 1: Definir os objetivos e o escopo da avaliação**

Validar os fluxos de interação definidos nos cenários de uso, identificar problemas de usabilidade e medir a eficácia dos usuários na conclusão de tarefas-chave da Plataforma de Testes e Validação de Modelos de IA.

---

### **Passo 2: Definir o perfil dos participantes**

Recrutar **6 usuários** baseados nas três personas do projeto:
- **2 Engenheiros de ML** (Perfil Paulo Andrade)
- **2 Gerentes de Segurança** (Perfil Ricardo Santos)
- **2 Gestoras de Projetos** (Perfil Fernanda Costa)

---

### **Passo 3: Definir as tarefas (cenários) que os participantes irão executar**

Com base nos cenários de interação documentados:

**Tarefa 1 (Engenheiro de ML):** Configurar modelo, executar análise e ordenar métricas  
**Tarefa 2 (Gerente de Segurança):** Consultar relatório específico e exportar em CSV  
**Tarefa 3 (Gestora de Projetos):** Identificar melhor modelo e exportar dados consolidados

---

### **Passo 4: Preparar e imprimir todos os instrumentos e materiais de apoio necessários**

- Termo de Consentimento Livre e Esclarecido (TCLE)
- Questionários Pré e Pós-Teste
- Roteiros de Tarefas impressos
- Tabelas de Observação
- Arquivos de teste (modelos .pt, vídeos)

---

### **Passo 5: Preparar o ambiente, hardware e software**

- Sala silenciosa com computador equipado com GPU NVIDIA
- Protótipo PyQt5 instalado e funcional
- Software de gravação de tela (OBS Studio)
- Cronômetro para registro de tempo

---

### **Passo 6: Realizar um teste-piloto**

Executar teste completo com um colega de equipe para validar o roteiro, identificar problemas nas tarefas e ajustar tempo estimado.

---

## Resultados do Teste

### **Avaliação de cada Tarefa (para cada usuário)**

| Tarefa | Grau de Sucesso | Total de Erros cometidos | Tipos de Erros | Tempo Necessário | Grau de Satisfação |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1 (P01 - Eng. ML)** | Sucesso Parcial | 3 | (1) Falha (não encontrou upload modelo), (1) Compreensão (limite confiança), (1) Hesitação (ordenar métricas) | 7 min 45 seg | Confusão Moderada |
| **2 (P02 - Ger. Seg.)** | Sucesso Total | 1 | (1) Hesitação (procurou por nome, estava por data) | 3 min 20 seg | Satisfeito |
| **3 (P03 - Gest. Proj.)** | Sucesso Total | 0 | N/A (Nenhum erro cometido) | 2 min 10 seg | Muito Satisfeita |
| **1 (P04 - Eng. ML)** | Falha | 4 | (1) Falha (não configurou GPU), (2) Recuperação (upload arquivo errado 2x), (1) Compreensão (métricas) | 9 min 30 seg | Muito Insatisfeito |
| **2 (P05 - Ger. Seg.)** | Sucesso Parcial | 2 | (1) Compreensão (não entendeu dashboards) | 4 min 55 seg | Neutro |
| **3 (P06 - Gest. Proj.)** | Sucesso Total | 1 | (1) Hesitação (comparou modelos manualmente) | 3 min 40 seg | Satisfeita |

---

### **Links dos Vídeos:**

### **Respostas do Formulário do Usuário:**

#### **Usuário P01 (Engenheiro ML - Tarefa 1)**

**Perfil (Pré-teste):**
- **Função:** Engenheiro de Machine Learning
- **Experiência:** 3 a 5 anos
- **Conforto com novas ferramentas (1-5):** 5

**Satisfação (Pós-teste):**
- **Achei o sistema fácil de usar (1-5):** 3 (Neutro)
- **As mensagens de erro me ajudaram (1-5):** 2 (Discordo)
- **O que foi mais difícil?** "Não achei onde fazer upload do modelo .pt. Procurei por 2 minutos na tela de análise antes de descobrir que era na tela de configurações. Também não entendi direito o que era 'limite de confiança'."
- **O que mudaria?** "Precisa ter um botão ou indicação mais clara de onde configurar o modelo. Talvez um wizard inicial ou tutorial. E colocar uma explicação (tooltip) no campo 'limite de confiança'."

---

#### **Usuário P02 (Gerente Seg. - Tarefa 2)**

**Perfil (Pré-teste):**
- **Função:** Coordenador de Segurança do Trabalho
- **Experiência:** Mais de 5 anos
- **Conforto com novas ferramentas (1-5):** 3

**Satisfação (Pós-teste):**
- **Achei o sistema fácil de usar (1-5):** 4 (Concordo)
- **As informações estavam claras e organizadas (1-5):** 5 (Concordo Totalmente)
- **O que foi mais fácil?** "A tabela de relatórios é bem organizada. Consegui achar rapidamente o que eu precisava. Exportar foi simples, só um clique."
- **O que mudaria?** "Adicionar busca por nome do modelo. Mas no geral, achei muito bom."

---

#### **Usuário P03 (Gestora Proj. - Tarefa 3)**

**Perfil (Pré-teste):**
- **Função:** Gestora de Projetos
- **Experiência:** 3 a 5 anos
- **Conforto com novas ferramentas (1-5):** 4

**Satisfação (Pós-teste):**
- **Achei o sistema fácil de usar (1-5):** 5 (Concordo Totalmente)
- **As informações estavam claras e organizadas (1-5):** 5 (Concordo Totalmente)
- **O que foi mais fácil?** "Tudo foi muito intuitivo. A interface é limpa, consegui navegar sem ajuda. A exportação em CSV foi perfeita."
- **O que mudaria?** "Seria ótimo ter uma tela de comparação lado a lado de múltiplos modelos, com gráficos."

---

#### **Usuário P04 (Engenheiro ML - Tarefa 1)**

**Perfil (Pré-teste):**
- **Função:** Cientista de Dados
- **Experiência:** 1 a 3 anos
- **Conforto com novas ferramentas (1-5):** 4

**Satisfação (Pós-teste):**
- **Achei o sistema fácil de usar (1-5):** 2 (Discordo)
- **As mensagens de erro me ajudaram (1-5):** 1 (Discordo Totalmente)
- **O que foi mais difícil?** "Tudo. Tentei fazer upload de um arquivo .txt por engano e o sistema aceitou — quando tentei rodar, deu erro genérico 'Falha no upload'. Depois tentei com o .pt mas esqueci de marcar 'Usar GPU'. Quando finalmente rodou, fiquei confuso com as métricas — mAP, IoU..."
- **O que mudaria?** "VALIDAÇÃO DE ARQUIVO é fundamental. O sistema não pode aceitar qualquer arquivo. Precisa de mensagens de erro claras. E as métricas precisam de explicação — um '?' do lado com tooltip."

---

#### **Usuário P05 (Gerente Seg. - Tarefa 2)**

**Perfil (Pré-teste):**
- **Função:** Gerente de Segurança do Trabalho
- **Experiência:** Mais de 5 anos
- **Conforto com novas ferramentas (1-5):** 2

**Satisfação (Pós-teste):**
- **Achei o sistema fácil de usar (1-5):** 3 (Neutro)
- **As informações estavam claras e organizadas (1-5):** 2 (Discordo)
- **O que foi mais difícil?** "Entender o que significam as métricas. Eu não sei o que é 'mAP' ou 'F1-Score'. Eu estava procurando algo como 'taxa de acerto'. Também demorei para achar o botão de exportar — ele está meio escondido."
- **O que mudaria?** "Traduzir as métricas para uma linguagem mais simples. E o botão de exportar poderia ser maior e mais visível."

---

#### **Usuário P06 (Gestora Proj. - Tarefa 3)**

**Perfil (Pré-teste):**
- **Função:** Engenheira de Obras
- **Experiência:** 1 a 3 anos
- **Conforto com novas ferramentas (1-5):** 4

**Satisfação (Pós-teste):**
- **Achei o sistema fácil de usar (1-5):** 4 (Concordo)
- **As informações estavam claras e organizadas (1-5):** 4 (Concordo)
- **O que foi mais fácil?** "A interface é bonita e organizada. Consegui navegar tranquilamente."
- **O que mudaria?** "Teria sido útil ter filtros para ordenar por 'melhor desempenho' ou alguma visualização comparativa."

---

## **Conclusão da Avaliação por Observação do Usuário**

### **Pontos Positivos (Sucessos):**

**Fluxos de Consulta e Exportação de Relatórios (Gerente e Gestora):**
- As tarefas de "Consultar e Exportar Relatório" (Gerente de Segurança - P02) e "Localizar e Exportar Dados" (Gestora de Projetos - P03 e P06) foram validadas com sucesso.
- **Alta Satisfação:** Os usuários P02, P03 e P06 classificaram essas tarefas como "fáceis" e "satisfatórias", destacando a clareza da organização e a simplicidade da exportação.
- **Eficiência:** P03 (Gestora) completou sua tarefa em apenas 2min 10seg sem erros, demonstrando alta eficiência da interface.

### **Pontos Críticos (Falhas):**

**Fluxo de Configuração e Execução de Análise (Engenheiro de ML):**
- A tarefa "Configurar e Executar Análise" (Engenheiro ML - P01 e P04) apresentou **falhas graves de usabilidade**, resultando em "Sucesso Parcial" ou "Falha Completa", confusão e insatisfação significativa.

**Principais Problemas Identificados:**

1. **Falta de Validação de Formato de Arquivo (Heurística 5):** 
   - O sistema aceitou arquivo .txt no upload de modelo sem validação, causando erro genérico "Falha no upload" (P04).
   - Violação crítica que pode comprometer funcionamento do sistema.

2. **Fluxo de Configuração Não-Intuitivo (Heurística 3):**
   - Ambos engenheiros (P01 e P04) procuraram por 2+ minutos onde fazer upload do modelo, esperando encontrar na tela de análise quando estava em configurações.
   - Falta de "saída de emergência" clara e fluxo guiado.

3. **Ausência de Tooltips Explicativos (Heurística 10):**
   - P01 não compreendeu "limite de confiança" e P04 ficou confuso com métricas técnicas (mAP, IoU, F1-Score).
   - Violação do princípio de ajuda e documentação.

4. **Mensagens de Erro Genéricas (Heurística 9):**
   - P04 recebeu erro "Falha no upload" sem explicação de que o arquivo não era .pt válido.
   - Mensagens não ajudaram na recuperação, gerando frustração (nota 1/5).

5. **Jargão Técnico para Perfis Não-Técnicos (Heurística 2):**
   - P05 (Gerente de Segurança) não compreendeu os Dashboards mostrados.
   - Compromete objetivo de Ricardo Santos avaliar confiabilidade dos modelos.

---
