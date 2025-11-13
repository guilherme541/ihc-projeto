# 1) Cenários de Interação

## Cenário de Interação A: Painel de Resultados (Ricardo Santos)

**Atores:** Ricardo Santos (Gerente de Segurança) e Fernanda Costa (Engenheira e Gestora de Obra)

Ricardo precisa avaliar o desempenho dos modelos de detecção utilizados pela empresa.  
Ele acessa o Painel de Resultados, onde visualiza dashboards com informações sobre o modelo utilizado, tempo de processamento, precisão e a distribuição de classes detectadas para o modelo selecionado.  
O sistema apresenta gráficos comparativos do relatório selecionado, onde possui uma opção para exportá-lo.

Ao clicar no botão "Exportar Resoltados (CSV/Excel)", ele exporta o relatório em CSV para poder realizar as devidas análises a partir das métricas contidas dentro do relatório, podendo decidir qual modelo teve melhor desempenho para detecção no ambiente de obra. 
Essa funcionalidade facilita a comunicação entre os setores e otimiza o processo de tomada de decisão para definir o modelo ideal para uso em campo.

---

## Cenário de Interação B: Análise de Modelos (Fernanda Costa)

**Atores:** João (Técnico de Segurança)

João deseja testar um novo modelo de detecção treinado recentemente.  
Ele acessa a tela de Análise, faz o upload do arquivo do modelo e clica em “Iniciar Testes”. 
O sistema processa o modelo configurado para detectar vídeos ou imagens e, ao final, apresenta as métricas obtidas.

Após a execução, João utiliza o filtro por métricas para visualizar apenas os modelos que superaram o limiar de confiança definido anteriormente. 
Assim, ele consegue utilizar um filtro para ordenar as métricas obtidas a partir da análise do modelo configurado, conseguindo, em tempo real, analisar o desempenho do modelo sendo testado em diversos contextos diferentes.

---

## Cenário de Interação C: Configurações do Modelo (João)

**Atores:** João (Técnico de Segurança)

João é responsável por preparar o ambiente de teste dos modelos.  
Na tela de Configurações do Modelo, ele consegue subir os modelos **.pt**, ou utilizar os que já estão na interface, e escolher se deseja utilizar a placa gráfica para acelerar o processamento e seleciona qual modelo será testado na próxima análise.  
Ele também define o limite de confiança mínimo para as detecções.

Após salvar as configurações, João inicia a execução do modelo na tela de Análise.  
Essas opções permitem um controle técnico refinado e garantem que os testes sejam executados conforme a capacidade dos equipamentos disponíveis.

---

# 2) Design Centrado na Comunicação

## Nome do Cenário: Painel de Resultados (Ricardo Santos) e (Fernanda Costa)

| tópico > subtópico (diálogo) | falas e signos |
| :---- | :---- |
| Acessar Painel de Resultados | U: Quero visualizar os relatórios dos modelos testados. |
| > Selecionar Relatório | U: Seleciona relatório existente no sistema. |
| > Visualizar dashboards | D: Exibindo métricas de desempenho e gráficos comparativos a partir do relatório selecionado. |
| > Exportar relatório | U: Exportar relatório do modelo YOLOv8. <br> D: Relatório exportado com sucesso em formato CSV. |

---

## Nome do Cenário: Análise de Modelos (João)

| tópico > subtópico (diálogo) | falas e signos |
| Acessar Análise | U: Quero realizar a análise de uma imagem ou vídeo a partir do modelo selecionado. |
| Fazer upload do arquivo | U: Seleciona arquivo de vídeo ou imagem. |
| > Iniciar Análise | D: Analisando... Isso pode levar alguns instantes. |
| > Filtrar métricas | U: Ordenar por métrica. <br> D: Exibindo resultados filtrados por ordem. |

---

## Nome do Cenário: Configurações do Modelo (João)

| tópico > subtópico (diálogo) | falas e signos |
| :---- | :---- |
| Selecionar hardware | U: Utilizar GPU para acelerar o teste. |
| > Escolher modelo | D: Modelo YOLOv8 selecionado. |
| > Definir limite de confiança | U: Ajustar limite de confiança para 0.85. <br> D: Configuração salva com sucesso. |

---

# 3) Mapa de Objetivos

**Descrição:**  
O mapa de objetivos demonstra como as funcionalidades da interface se alinham com as metas de cada persona:  
- **Ricardo (Gerente de Segurança):** Avaliar o desempenho dos modelos e exportar relatórios consolidados para apoio na decisão estratégica.  
- **Fernanda (Engenheira de Obra):** Testar e comparar modelos em diferentes contextos visuais, filtrando resultados conforme métricas de desempenho.  
- **João (Técnico de Segurança):** Configurar corretamente o ambiente de análise, garantindo eficiência e estabilidade nos testes.  

O objetivo central é **permitir que as empresas desenvolvedoras testem e escolham o melhor modelo de detecção para ambientes de obra**, promovendo precisão, eficiência e confiabilidade nos resultados.

---

# 4) Esquema Conceitual de Signos

| Usuário do Sistema (US) - Credenciais e perfil de acesso | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção / recuperação** |
| + id_usuario | aplicação | Identificador único. | texto | não pode ser nulo, único | gerado automaticamente | N/A |
| nome | domínio | Nome completo. | texto | não pode ser nulo | — | **PP:** campo obrigatório |
| cargo | domínio | Define o perfil: Gerente, Engenheira, Técnico. | seleção simples | {Gerente, Engenheira, Técnico} | — | **PA:** seleção obrigatória |
| email_login | domínio | E-mail corporativo. | texto | formato válido | — | **PP+PA:** validação de formato |
| senha | aplicação | Credencial criptografada. | texto | mínimo 8 caracteres | — | **PP:** regras de complexidade |

---

| Modelo (ML) - Algoritmos de detecção em teste | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção / recuperação** |
| + id_modelo | aplicação | Identificador único do modelo. | texto | não pode ser nulo, único | — | **PP:** validação de ID |
| nome_modelo | domínio | Nome do modelo carregado. | texto | não pode ser nulo | — | **PP:** campo obrigatório |
| versao | domínio | Versão do modelo. | texto | — | — | — |
| tipo_treinamento | domínio | Define se o modelo foi treinado com imagens reais, sintéticas ou mistas. | seleção simples | {Reais, Sintéticas, Reais+Sintéticas} | — | **PA:** validação automática |
| limite_confianca | aplicação | Valor mínimo de confiança definido pelo usuário. | número | ≥ 0 e ≤ 1 | 0.5 | **PA:** ajuste automático |

---

| Relatório (RT) - Resultados das análises executadas | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção / recuperação** |
| + id_relatorio | aplicação | Identificador único. | texto | não pode ser nulo, único | gerado automaticamente | N/A |
| data_execucao | domínio | Data em que o teste foi executado. | data | não pode ser nula | data atual | **PP+PA:** seletor automático |
| modelo_utilizado | domínio | Nome do modelo testado. | texto | não pode ser nulo | — | **PP:** campo obrigatório |
| metrica_principal | aplicação | Métrica de desempenho principal (ex: mAP). | número | ≥ 0 e ≤ 100 | — | **PA:** preenchido automaticamente |
| arquivo_relatorio | aplicação | Caminho do arquivo PDF exportado. | texto | — | — | **RA:** reexportar em caso de falha |
