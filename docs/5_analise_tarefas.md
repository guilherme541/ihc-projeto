# Análise de Tarefas

> **_NOTE:_**: A equipe deve descrever as funcionalidades mais importantes da interface/produto. A equipe deve modelar pelo menos 1 HTA, 1 GOMS e 1 CTT (de pelo menos 4 funcionalidades diferentes). Cada diagrama deve ter um texto explicando a funcionalidade.

1. HTA  
3. GOMS
4. CTT


## 1. Registro de Usuário

<img width="943" height="594" alt="Untitled Diagram drawio (7)" src="https://github.com/user-attachments/assets/42791815-e421-4ffb-b6ce-863805b509ca" />



| Objetivos/Operações                                | Problemas e Recomendações |
|---|---|
| 0. Registro de um novo usuário 1>2                 | Input: Um novo possível usuário acessa a página para criar um registro.<br>Feedback: usuário confirma os dados, a conta é criada e um e‑mail de confirmação do registro é enviado.<br>Plano: executar a operação 1 e depois a 2. |
| 1. Informar dados do usuário 1+2                   | Plano: (1.1) informar nome e e‑mail; (1.2) aceitar termos e autorizações necessárias.<br>Risco geral: campos obrigatórios pouco claros e validações tardias aumentam retrabalho.<br>Recomendação geral: validação em tempo real e mensagens objetivas junto aos campos. |
| 1.1 Informar nome e e‑mail                         | Problema: e‑mail inválido ou já cadastrado; campo obrigatório não destacado.<br>Recomendação: validação de formato e duplicidade em tempo real; indicação visual de obrigatórios e mensagens de erro claras. |
| 1.2 Aceitar termos e autorizações                  | Problema: usuário tenta prosseguir sem aceitar os termos.<br>Recomendação: bloquear avanço sem aceite, exibir aviso claro e link para visualizar os termos. |

| 2. Confirmar cadastro e notificar o usuário        | Problema: usuário não percebe o sucesso ou não sabe o próximo passo.<br>Recomendação: mensagem de sucesso clara e persistente, resumo do cadastro e envio de e‑mail de confirmação com instruções para o primeiro acesso. |

## GOMS

- **GOAL 0:** Registro de um novo usuário  

  - **GOAL 1:** Informar dados do usuário  
    - **METHOD 1.A:** Preencher formulário de cadastro  
      - (SEL. RULE: O usuário acessa a página de registro do sistema)
      - **OP. 1.A.1:** Tocar no campo “Nome”  
      - **OP. 1.A.2:** Digitar o nome completo  
      - **OP. 1.A.3:** Tocar no campo “E‑mail”  
      - **OP. 1.A.4:** Digitar o endereço de e‑mail válido  
      - **OP. 1.A.5:** Tocar no campo “Senha”  
      - **OP. 1.A.6:** Digitar a senha desejada  
      - **OP. 1.A.7:** Tocar no campo “Confirmar senha”  
      - **OP. 1.A.8:** Digitar novamente a senha desejada  
      - **OP. 1.A.9:** Clicar em “Próximo passo”

  - **GOAL 1.2:** Aceitar termos e autorizações  
    - **METHOD 1.B:** Ler e aceitar os termos de uso  
      - (SEL. RULE: O usuário deve aceitar os termos antes de concluir o cadastro)
      - **OP. 1.B.1:** Rolar a tela até o final dos termos  
      - **OP. 1.B.2:** Marcar a caixa “Li e aceito os termos”  
      - **OP. 1.B.3:** Clicar no botão “Concluir cadastro”  

  - **GOAL 2:** Confirmar cadastro e notificar o usuário  
    - **METHOD 2.A:** Confirmar criação da conta  
      - (SEL. RULE: Todos os campos foram preenchidos corretamente e os termos aceitos)
      - **OP. 2.A.1:** O sistema valida os dados inseridos  
      - **OP. 2.A.2:** O sistema cria o registro do usuário no banco  
      - **OP. 2.A.3:** O sistema exibe a mensagem “Cadastro concluído com sucesso”  
      - **OP. 2.A.4:** O sistema envia o e‑mail de confirmação ao usuário  
      - **OP. 2.A.5:** Usuário lê a mensagem e clica em “Acessar conta”

## CTT

<img width="966" height="737" alt="Untitled Diagram drawio (6)" src="https://github.com/user-attachments/assets/d21af784-1f51-4a80-af14-ceb74383fac3" />

## 2.Carregar arquivo e detectar objetos

<img width="1080" height="561" alt="Untitled Diagram drawio (11)" src="https://github.com/user-attachments/assets/ad1e1b57-49e8-4c79-9c20-554fbb4b3e62" />


| **Objetivos/Operações**                            | **Problemas e Recomendações**                                                                                              |
|---|---|
| 0. Carregar arquivo e detectar objetos 1>2     | Input: O usuário inicia a tarefa de detecção de objetos em um arquivo.<br>Feedback: Objetos detectados exibidos na tela.<br>Plano: Realizar a operação 1 e depois a 2.<br>Recomendação: Garantir feedback visual claro durante o processamento e salvar o resultado. |
| 1. Iniciar a detecção de objetos 1+2               | Plano: Selecionar tipo de detecção, escolher modelo e carregar imagem antes de iniciar detecção.                              |
| 1.1 Informar o modelo de detecção                   | Problema: Lista de modelos pode ser confusa para usuários iniciantes.<br>Recomendação: Incluir descrição breve para cada modelo. |
| 1.2 Enviar imagem para o sistema                    | Problema: Formatos incompatíveis ou arquivos corrompidos podem causar falha.<br>Recomendação: Validar formatos e exibir mensagens claras. |
| 2. Salvar o resultado                               | Plano: Salvar arquivo após detecção.<br>Problema: Usuário pode não encontrar arquivo salvo.<br>Recomendação: Mostrar caminho e opção para abrir pasta. |

## GOMS 

**GOAL 0:** Detectar objetos em um arquivo

- **GOAL 1:** Carregar arquivo para detecção  
  - **METHOD 1.A:** Selecionar arquivo de imagem  
    - **OP. 1.A.1:** Abrir diálogo de seleção de arquivo  
    - **OP. 1.A.2:** Navegar até o arquivo desejado  
    - **OP. 1.A.3:** Selecionar arquivo e confirmar  
  - **METHOD 1.B:** Validar formato e integridade do arquivo  
    - **OP. 1.B.1:** Verificar extensão do arquivo (imagem e video) 
    - **OP. 1.B.2:** Verificar integridade do arquivo  
    - **SELECTION RULE:** Se arquivo inválido, exibir mensagem de erro e solicitar novo arquivo  

- **GOAL 2:** Iniciar detecção de objetos  
  - **METHOD 2.A:** Escolher modelo de detecção  
    - **OP. 2.A.1:** Exibir lista de modelos  
    - **OP. 2.A.2:** Ler descrição do modelo (se necessário)  
    - **OP. 2.A.3:** Selecionar modelo  
  - **METHOD 2.B:** Enviar imagem para o sistema  
    - **OP. 2.B.1:** Confirmar envio da imagem  
    - **OP. 2.B.2:** Aguardar processamento  
    - **SELECTION RULE:** Se falha no envio, exibir mensagem e permitir reenvio  

- **GOAL 3:** Salvar resultado  
  - **METHOD 3.A:** Salvar resultado em arquivo  
    - **OP. 3.B.1:** Abrir diálogo de salvar arquivo  
    - **OP. 3.B.2:** Confirmar local e nome do arquivo  
    - **OP. 3.B.3:** Salvar arquivo  
    - **SELECTION RULE:** Se usuário não encontrar arquivo, mostrar caminho e opção para abrir pasta
   
## CTT
![Untitled Diagram](https://github.com/user-attachments/assets/7fb615fd-42a6-4227-acce-54a06f71e8e0)


## 3. Exportar Relátorio de Detecção

<img width="2137" height="654" alt="Untitled Diagram drawio (12)" src="https://github.com/user-attachments/assets/94ac99f5-54f7-43e1-9b63-a632ed2b4c71" />


| Objetivos/Operações | Problemas e Recomendações |
|:-------------------|:--------------------------|
| **0. Exportar Relatório de Detecção 1>2>3** | **Input:** dados do relatório, modelos, períodos e classes<br>**Feedback:** relatório gerado e exportado com sucesso<br>**Plano:** definir dados do relatório, depois gerar relatório e depois exportar dados |
| **1. Definir dados do relatório 1+2+3** | **Plano:** selecionar o modelo, selecionar o período e selecionar o tipo de classes em paralelo |
| 1.1 Selecionar o Modelo | |
| 1.2 Selecionar o Período | |
| 1.3 Selecionar o tipo de classes | |
| **2. Exportar Relatório 1+2** | **Plano:** selecionar o formato de saída e visualizar prévia dos dados simultaneamente |
| 2.1 Selecionar o formato de saída | |
| 2.2 Visualizar Prévia dos dados | |
| **3. Exportar Dados** | |

## GOMS

- **GOAL 0:** Exportar Relatório de Detecção  

  - **GOAL 1:** Definir dados do relatório  
    - **METHOD 1.A:** Preencher filtros do relatório  
      - (SEL. RULE: O usuário acessa a tela de geração de relatórios de detecção)  
      - **OP. 1.A.1:** Clicar no campo "Modelo"  
      - **OP. 1.A.2:** Selecionar o modelo desejado na lista  
      - **OP. 1.A.3:** Clicar no campo de "Data inicial"  
      - **OP. 1.A.4:** Escolher a data inicial no calendário  
      - **OP. 1.A.5:** Clicar no campo de "Data final"  
      - **OP. 1.A.6:** Escolher a data final no calendário  
      - **OP. 1.A.7:** Examinar a lista de tipos de classes disponíveis  
      - **OP. 1.A.8:** Marcar/desmarcar as classes desejadas  
      - **OP. 1.A.9:** Clicar em "Aplicar filtros"  

  - **GOAL 2:** Exportar Relatório  
    - **METHOD 2.A:** Configurar saída e visualizar prévia  
      - (SEL. RULE: Os filtros de modelo, período e classes já foram definidos)  
      - **OP. 2.A.1:** Clicar no campo "Formato de saída"  
      - **OP. 2.A.2:** Selecionar o formato desejado (por exemplo, "Tabela na tela", "PDF" ou "CSV")  
      - **OP. 2.A.3:** Clicar no botão "Gerar" / "Visualizar"  
      - **OP. 2.A.4:** Analisar a prévia dos dados apresentada  
      - **OP. 2.A.5:** Verificar se o conteúdo está de acordo com o esperado  
      - **OP. 2.A.6:** Caso a prévia não esteja correta, retornar ao **GOAL 1** para ajustar filtros  

  - **GOAL 3:** Exportar dados  
    - **METHOD 3.A:** Exportar o relatório gerado  
      - (SEL. RULE: A prévia do relatório foi validada pelo usuário)  
      - **OP. 3.A.1:** Clicar no botão "Exportar"  
      - **OP. 3.A.2:** Selecionar o formato de exportação (CSV, XLSX, PDF, etc.)  
      - **OP. 3.A.3:** Escolher o local de salvamento do arquivo  
      - **OP. 3.A.4:** Confirmar a ação de exportar  
      - **OP. 3.A.5:** Aguardar a conclusão da exportação e verificar se o arquivo foi criado corretamente

## CTT
![Untitled Diagram (1)](https://github.com/user-attachments/assets/e75077ca-9a6d-4954-a897-74daa606d93d)


## 4. Configuração do Modelo
![Untitled Diagram (2)](https://github.com/user-attachments/assets/d9092d4f-adf3-466d-9a78-7e4a4bcf076d)

| Objetivos/Operações | Problemas e Recomendações |
|:--------------------|:--------------------------|
| **0. Configurar o Modelo 1>2>3** | **Input:** tela de configuração de modelo, com campos de processamento, seleção de modelo e opção de salvar.<br>**Feedback:** configuração salva e aplicada ao sistema/modelo.<br>**Plano:** primeiro definir informação sobre processamento, depois selecionar o modelo e por fim salvar a configuração. |
| **1. Definir informação sobre processamento 1/2** | **Plano:** o usuário pode informar apenas CPU, apenas GPU ou ambas, conforme o ambiente de execução. |
| 1.1 Informar CPU | *Possível problema:* campo técnico demais para usuários leigos (número de núcleos, threads, etc.).<br>*Recomendação:* oferecer ajuda contextual (ícones de ajuda, exemplos de preenchimento ou valores padrão sugeridos). |
| 1.2 Informar GPU | *Possível problema:* usuário pode não saber o modelo ou memória da GPU disponível.<br>*Recomendação:* permitir detecção automática do hardware ou exibir uma lista das GPUs detectadas para seleção. |
| **2. Selecionar o modelo** | *Recomendações:* permitir busca por nome, filtros (desempenho) e descrição resumida de cada modelo. |
| **3. Salvar configuração** | *Possíveis problemas:* usuário não tem certeza se as alterações foram realmente aplicadas ou se substituirão uma configuração anterior.<br>*Recomendações:* exibir mensagem de confirmação (“Configuração salva com sucesso”), indicar qual configuração está ativa no momento e oferecer opção de salvar como novo perfil sem sobrescrever os anteriores. |



