# Análise de Tarefas

> **_NOTE:_**: A equipe deve descrever as funcionalidades mais importantes da interface/produto. A equipe deve modelar pelo menos 1 HTA, 1 GOMS e 1 CTT (de pelo menos 4 funcionalidades diferentes). Cada diagrama deve ter um texto explicando a funcionalidade.

1. HTA  
3. GOMS
4. CTT


## 1. Registro de Usuário


<img width="943" height="594" alt="Untitled Diagram drawio (4)" src="https://github.com/user-attachments/assets/32821dd6-d1ae-4a28-8295-679d00fa467f" />


| Objetivos/Operações                                | Problemas e Recomendações |
|---|---|
| 0. Registro de um novo usuário 1>2                 | Input: Um novo possível usuário acessa a página para criar um registro.<br>Feedback: usuário confirma os dados, a conta é criada e um e‑mail de confirmação do registro é enviado.<br>Plano: executar a operação 1 e depois a 2. |
| 1. Informar dados do usuário 1+2                   | Plano: (1.1) informar nome e e‑mail; (1.2) aceitar termos e autorizações necessárias.<br>Risco geral: campos obrigatórios pouco claros e validações tardias aumentam retrabalho.<br>Recomendação geral: validação em tempo real e mensagens objetivas junto aos campos. |
| 1.1 Informar nome e e‑mail                         | Problema: e‑mail inválido ou já cadastrado; campo obrigatório não destacado.<br>Recomendação: validação de formato e duplicidade em tempo real; indicação visual de obrigatórios e mensagens de erro claras. |
| 1.2 Aceitar termos e autorizações                  | Problema: usuário tenta prosseguir sem aceitar os termos.<br>Recomendação: bloquear avanço sem aceite, exibir aviso claro e link para visualizar os termos. |
| 2. Confirmar cadastro e notificar o usuário        | Problema: usuário não percebe o sucesso ou não sabe o próximo passo.<br>Recomendação: mensagem de sucesso clara e persistente, resumo do cadastro e envio de e‑mail de confirmação com instruções para o primeiro acesso. |
