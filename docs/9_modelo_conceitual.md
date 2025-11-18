# 1) Cenários de Interação

## Cenário de Interação A: Painel de Resultados

**Atores:** Ricardo Santos e Fernanda Costa

Ricardo precisa avaliar o desempenho dos modelos de detecção utilizados pela empresa.  
Ele acessa o Painel de Resultados, onde visualiza dashboards com informações sobre o modelo utilizado, tempo de processamento, precisão e a distribuição de classes detectadas para o modelo selecionado.  
O sistema apresenta gráficos comparativos do relatório selecionado, onde possui uma opção para exportá-lo.

Ao clicar no botão "Exportar Resoltados (CSV/Excel)", ele exporta o relatório em CSV para poder realizar as devidas análises a partir das métricas contidas dentro do relatório, podendo decidir qual modelo teve melhor desempenho para detecção no ambiente de obra. 
Essa funcionalidade facilita a comunicação entre os setores e otimiza o processo de tomada de decisão para definir o modelo ideal para uso em campo.

---

## Cenário de Interação B: Análise de Modelos

**Atores:** Paulo Andrade

Paulo deseja testar um novo modelo de detecção treinado recentemente.  
Ele acessa a tela de Análise, faz o upload do arquivo do modelo e clica em “Iniciar Testes”. 
O sistema processa o modelo configurado para detectar vídeos ou imagens e, ao final, apresenta as métricas obtidas.

Após a execução, Paulo utiliza o filtro por métricas para visualizar apenas os modelos que superaram o limiar de confiança definido anteriormente. 
Assim, ele consegue utilizar um filtro para ordenar as métricas obtidas a partir da análise do modelo configurado, conseguindo, em tempo real, analisar o desempenho do modelo sendo testado em diversos contextos diferentes.

---

## Cenário de Interação C: Configurações do Modelo

**Atores:** Paulo Andrade

Paulo é responsável por preparar o ambiente de teste dos modelos.  
Na tela de Configurações do Modelo, ele consegue subir os modelos **.pt**, ou utilizar os que já estão na interface, e escolher se deseja utilizar a placa gráfica para acelerar o processamento e seleciona qual modelo será testado na próxima análise.  
Ele também define o limite de confiança mínimo para as detecções.

Após salvar as configurações, Paulo inicia a execução do modelo na tela de Análise.  
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

## Nome do Cenário: Análise de Modelos (Paulo Andrade)

| tópico > subtópico (diálogo) | falas e signos |
| :---- | :---- |
| Acessar Análise | U: Quero realizar a análise de uma imagem ou vídeo a partir do modelo selecionado. |
| Fazer upload do arquivo | U: Seleciona arquivo de vídeo ou imagem. |
| > Iniciar Análise | D: Analisando... Isso pode levar alguns instantes. |
| > Filtrar métricas | U: Ordenar por métrica. <br> D: Exibindo resultados filtrados por ordem. |

---

## Nome do Cenário: Configurações do Modelo (Paulo Andrade)

| tópico > subtópico (diálogo) | falas e signos |
| :---- | :---- |
| Configurar o modelo | U: Desejo subir um modelo novo ou utilizar algum existente. |
| > Escolher modelo | D: Modelo YOLOv8 carregado ou selecionado. |
| Selecionar hardware | U: Desejo utilizar GPU para acelerar os testes. |
| Limite de confiança | U: Desejo definir os limites de confiança para os testes. |
| > Definir limite de confiança | U: Ajustar limite de confiança para 0.85. <br> D: Configuração salva com sucesso. |

---

# 3) Mapa de Objetivos



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
| limite_confianca | aplicação | Valor mínimo de confiança definido pelo usuário. | número | ≥ 0 e ≤ 1 | 0.5 | **PA:** ajuste manual |

---

| Relatório (RT) - Resultados das análises executadas | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **signo** | **origem** | **observações** | **Tipo de conteúdo** | **restrição sobre conteúdo** | **valor default** | **prevenção / recuperação** |
| + id_relatorio | aplicação | Identificador único. | texto | não pode ser nulo, único | gerado automaticamente | N/A |
| data_execucao | domínio | Data em que o teste foi executado. | data | não pode ser nula | data atual | **PP+PA:** seletor automático |
| modelo_utilizado | domínio | Nome do modelo testado. | texto | não pode ser nulo | — | **PP:** campo obrigatório |
| metrica_principal | aplicação | Métrica de desempenho principal (ex: mAP). | número | ≥ 0 e ≤ 100 | — | **PA:** preenchido automaticamente |
| arquivo_relatorio | aplicação | Caminho do arquivo CSV exportado. | texto | — | — | **RA:** reexportar em caso de falha |

| Análise (AN) - Execução e Avaliação de Modelos |            |                                                              |                      |                                    |                        |                                      |
| :--------------------------------------------- | :--------- | :----------------------------------------------------------- | :------------------- | :--------------------------------- | :--------------------- | :----------------------------------- |
| **signo**                                      | **origem** | **observações**                                              | **Tipo de conteúdo** | **restrição sobre conteúdo**       | **valor default**      | **prevenção / recuperação**          |
| + id_analise                                   | aplicação  | Identificador único da análise executada.                    | texto                | não pode ser nulo, único           | gerado automaticamente | N/A                                  |
| dataset                                        | domínio    | Arquivo de imagem ou vídeo enviado para análise.             | arquivo              | formatos aceitos: .jpg, .png, .mp4 | —                      | **PA:** validação de tipo de arquivo |
| tempo_execucao                                 | aplicação  | Tempo total gasto na análise.                                | float                | ≥ 0                                | —                      | **PA:** calculado automaticamente    |
| status                                         | aplicação  | Estado atual do processo de análise.                         | texto                | {Analisando..., Concluída, Erro}   | Analisando...          | **PA:** atualizado dinamicamente     |
| resultados                                     | aplicação  | Gráfico mostrando as métricas obtidas                        | texto                | —                                  | —                      | **PA:** preenchido após conclusão    |
| metricas_filtradas                             | domínio    | Ordenação por métricas.                                      | seleção múltipla     | {Ordenar por Confiança, Ordenar por desempenho}| Ordenar por Confiança | **PA:** filtragem por seleção        |

