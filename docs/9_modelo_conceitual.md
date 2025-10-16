# 1) Cenários de Interação

## Cenário de Interação A: Análise de Risco e Relatórios (Ricardo Santos)

**Atores:** Ricardo Santos (Gerente de Segurança)

Ricardo precisa apresentar à diretoria um relatório sobre os riscos identificados nas últimas semanas no canteiro de obras.  
**Com o novo sistema de monitoramento por drones, ele acessa o painel “Gestão de Segurança” e seleciona o módulo “Análise de Riscos Automatizada”.**  
O sistema carrega relatórios diários enviados pelos drones e pela equipe de campo. Ricardo filtra os dados por período e local, obtendo uma visão consolidada das áreas com maior índice de perigo.

**Em poucos cliques, ele visualiza gráficos de risco, alertas por zona e um mapa de calor indicando as regiões críticas.**  
O sistema também sugere medidas preventivas com base em análises anteriores da IA. Ricardo pode gerar um relatório em PDF e compartilhá-lo diretamente com a equipe de gestão, economizando horas de trabalho manual e aumentando a precisão das decisões estratégicas.

---

## Cenário de Interação B: Monitoramento Operacional em Tempo Real (Fernanda Costa)

**Atores:** Fernanda Costa (Engenheira e Gestora de Obra)

Fernanda está acompanhando o andamento da obra e precisa verificar se há riscos de colisão entre escavadeiras e operários durante o turno.  
**Ela acessa o módulo “Monitoramento em Tempo Real” do sistema e visualiza, em um painel unificado, os feeds de drones sobre o canteiro.**  
O sistema destaca automaticamente zonas de proximidade perigosa entre máquinas e trabalhadores usando contornos vermelhos sobre o mapa.

**Fernanda utiliza o recurso “Analisar Evento” para ampliar a área crítica e visualizar as trajetórias dos equipamentos.**  
Com base nisso, ela define uma nova zona de segurança e envia uma notificação imediata à equipe de campo.  
O sistema registra a ação e atualiza o mapa de risco com o novo perímetro seguro, permitindo decisões rápidas e assertivas, sem interromper o cronograma da obra.

---

## Cenário de Interação C: Inspeção e Relato de Ocorrências (João)

**Atores:** João (Técnico de Segurança)

João é responsável por realizar vistorias periódicas no canteiro.  
**Ele inicia o voo do drone através da interface móvel do sistema. A IA embarcada identifica automaticamente movimentações anômalas, como operários sem EPI ou áreas com excesso de poeira.**  
Durante o voo, João recebe alertas visuais e sonoros na tela e pode capturar imagens ou vídeos com um toque.

**Após concluir o voo, o sistema gera automaticamente um relatório de inspeção com as imagens registradas e a classificação de risco de cada evento detectado.**  
João revisa o relatório, adiciona observações e envia o documento ao gerente Ricardo e à engenheira Fernanda, garantindo comunicação rápida e precisa entre os níveis operacional e gerencial.

---

# 2) Design Centrado na Comunicação

## Nome do Cenário: Análise de Risco e Relatórios (Ricardo Santos)

| tópico \> subtópico (diálogo) | falas e signos |
| :---- | :---- |
| Acessar painel de segurança | U: Preciso gerar um relatório consolidado de riscos do último mês. |
| > Filtrar e visualizar dados | D: Aqui estão as zonas de risco registradas pelos drones. Você pode aplicar filtros por data e local. |
| > Gerar relatório | U: Quero exportar o relatório completo com as recomendações da IA. <br> D: Relatório gerado com sucesso. O arquivo PDF está disponível para download. |

---

## Nome do Cenário: Monitoramento Operacional em Tempo Real (Fernanda Costa)

| tópico \> subtópico (diálogo) | falas e signos |
| :---- | :---- |
| Monitorar obra em tempo real | U: Mostrar as zonas de risco atuais no canteiro. |
| > Visualizar câmeras e drones | D: Exibindo os feeds ao vivo e os pontos de alerta ativos. |
| Analisar evento | U: Ampliar área de risco próxima à escavadeira. |
| > Gerar ação preventiva | D: Área selecionada. Deseja definir um novo perímetro de segurança? |
| > Confirmar atualização | U: Sim, ajustar limite para 8 metros. <br> D: Zona de segurança atualizada com sucesso. |

---

## Nome do Cenário: Inspeção e Relato de Ocorrências (João)

| tópico \> subtópico (diálogo) | falas e signos |
| :---- | :---- |
| Iniciar voo de inspeção | U: Iniciar verificação da área leste do canteiro. |
| > Capturar imagens e alertas | D: Drone em voo. Foram detectados 3 operários sem capacete. |
| > Revisar relatório automático | U: Adicionar observações e confirmar envio. <br> D: Relatório enviado ao Gerente de Segurança e à Engenheira de Obra. |

---

# 3) Mapa de Objetivos

------

**Descrição:**
O mapa de objetivos representa como as funcionalidades do sistema se conectam aos objetivos de cada persona:
- **Ricardo (Gerente de Segurança):** Busca consolidar dados de risco e obter relatórios estratégicos.  
- **Fernanda (Engenheira):** Visa monitorar e ajustar o ambiente para evitar acidentes.  
- **João (Técnico de Segurança):** Atua na detecção operacional e coleta de informações de campo.  

Esses objetivos se unem em torno do propósito central: **garantir a segurança no canteiro de obras por meio de monitoramento inteligente e comunicação integrada.**

---

# 4) Esquema Conceitual de Signos

| Usuário do Sistema (US) - Credenciais e perfil de acesso ao sistema | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção / recuperação** |
| + id_usuario | aplicação | Identificador único do usuário. | texto | não pode ser nulo, único | gerado automaticamente | N/A |
| nome | domínio | Nome completo do colaborador. | texto | não pode ser nulo | — | **PP:** campo obrigatório |
| cargo | domínio | Define o perfil: Gerente, Engenheira, Técnico. | seleção simples | {Gerente, Engenheira, Técnico} | — | **PA:** seleção obrigatória |
| email_login | domínio | E-mail corporativo para login. | texto | formato de e-mail válido | — | **PP+PA:** validação de formato |
| senha | aplicação | Credencial criptografada. | texto | mínimo 8 caracteres | — | **PP:** regras de complexidade |

---

| Drone (DR) - Equipamento de monitoramento aéreo | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção / recuperação** |
| + id_drone | domínio | Identificador único do drone. | texto | não pode ser nulo, único | — | **PP:** validação de ID |
| status | aplicação | Estado atual do drone. | texto | {Em voo, Em espera, Offline} | Em espera | **PA:** atualização automática |
| bateria | aplicação | Nível de energia restante. | número | ≥ 0 e ≤ 100 | — | **PA:** alerta abaixo de 15% |
| area_monitorada | domínio | Local do voo atual. | texto | não pode ser nulo | — | **PP:** campo obrigatório |

---

| Relatório de Inspeção (RI) - Registro de eventos e riscos detectados | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção / recuperação** |
| + id_relatorio | aplicação | Identificador único. | texto | não pode ser nulo, único | gerado automaticamente | N/A |
| data | domínio | Data da inspeção. | data | não pode ser nula | data atual | **PP+PA:** seletor de data |
| area | domínio | Local da ocorrência. | texto | não pode ser nulo | — | **PP:** campo obrigatório |
| descricao_evento | domínio | Observações do técnico. | texto | — | — | **RA:** campo de edição pós-inspeção |
| risco_classificado | aplicação | Avaliação feita pela IA. | seleção simples | {Baixo, Médio, Alto} | — | **PA:** preenchido automaticamente |

---

