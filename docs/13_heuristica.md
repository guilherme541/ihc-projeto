# Avaliação Heurística

<p align="center">
  <img src="https://github.com/user-attachments/assets/2ff79c3b-85d5-41a8-a103-e310d790c87a" alt="Tela geral de avaliação heurística" width="800" height="400"/>
</p>

---

## Metodologia

Esta avaliação heurística foi realizada com base nas **10 Heurísticas de Usabilidade de Nielsen (1994)**, aplicadas ao protótipo de média/alta fidelidade da **Plataforma de Testes e Validação de Modelos de IA para Segurança em Canteiros de Obras**.

### Escala de Severidade

| Grau | Tipo | Descrição |
|------|------|-----------|
| 0 | Sem importância | Não afeta a operação da interface |
| 1 | Cosmético | Não há necessidade imediata de solução |
| 2 | Simples | Problema de baixa prioridade (pode ser reparado) |
| 3 | Grave | Problema de alta prioridade (deve ser reparado) |
| 4 | Catastrófico | Muito grave, deve ser reparado de qualquer forma |

---

## Violações Identificadas

### Heurística 3 – Controle e Liberdade para o Usuário

<p align="center">
  <img width="1392" height="656" alt="image" src="https://github.com/user-attachments/assets/4e3954d2-cbc2-425c-bc8f-1d564caf8756" />
</p>

**Problema:** Impossibilidade de cancelar análise em andamento  
**Severidade:** 3 - Grave  
**Descrição:** Não há botão para cancelar/pausar processamento. Se usuário selecionou arquivo errado, precisa esperar conclusão (pode levar minutos/horas).

**Recomendação:**
- Adicionar botão "Cancelar Análise"
- Confirmação: "Tem certeza? O progresso será perdido"
- Limpar resultados parciais ao cancelar

> 💡 **Observação:** Esta funcionalidade é crítica para Paulo Andrade (Engenheiro de ML) que realiza testes diários e precisa de agilidade.

---

### Heurística 5 – Prevenção de Erros

<p align="center">
  <img width="1392" height="655" alt="image" src="https://github.com/user-attachments/assets/3d716df4-e8dc-4a6f-8349-828ef1c37a78" />
</p>

**Problema:** Falta de validação de formato de arquivo ao fazer upload de modelo  
**Severidade:** 4 - Catastrófico  
**Descrição:** Sistema aceita qualquer tipo de arquivo no campo "Selecionar Modelo" sem validar se é .pt válido. Pode causar crash ou corrupção de configurações.

**Recomendação:**
- Restringir seleção apenas para arquivos .pt
- Validar formato após seleção
- Mensagem clara: "Formato inválido. Selecione um arquivo .pt (modelo PyTorch)"
- Prevenir salvamento com arquivo inválido

> 💡 **Observação:** Este é um problema crítico que pode comprometer todo o funcionamento do sistema.

---

### Heurística 6 – Reconhecimento em Lugar de Lembrança

<p align="center">
  <img width="1392" height="659" alt="image" src="https://github.com/user-attachments/assets/8e8114d3-618c-4a7c-a799-99c0e8cece88" />
</p>

**Problema:** Dificuldade em identificar relatórios sem preview visual  
**Severidade:** 2 - Simples  
**Descrição:** Usuário precisa lembrar qual modelo foi testado, em qual data e com qual dataset. Não há thumbnail ou resumo visual para reconhecimento rápido.

**Recomendação:**
- Adicionar thumbnail do vídeo/imagem testada
- Tags visuais: "Alta Precisão", "Aprovado"
- Preview expandido ao passar mouse

> 💡 **Observação:** Este problema afeta principalmente a eficiência de usuários que executam múltiplos testes. Ricardo Santos revisa relatórios semanalmente e Fernanda Costa precisa localizar rapidamente dados para apresentações executivas. Preview visual economizaria tempo e reduziria frustração.
---

### Heurística 7 – Flexibilidade e Eficiência de Uso

<p align="center">
  <img width="1393" height="661" alt="image" src="https://github.com/user-attachments/assets/42d935f9-43da-4ede-acaf-432fa242aad6" />
</p>

**Problema:** Ausência de filtros avançados 
**Severidade:** 2 - Simples  
**Descrição:** Não há filtros refinados para usuários experientes. Paulo Andrade (uso diário) poderia ser mais produtivo com ferramentas avançadas.

**Recomendação:**
- Filtros múltiplos: data, modelo, tipo de arquivo, métricas mínimas
- Busca por nome
- Salvar filtros favoritos

> 💡 **Observação:** Usuários experientes precisam de caminhos rápidos para tarefas frequentes.

---

### Heurística 9 – Auxiliar Usuários a Reconhecer, Diagnosticar e Recuperar Erros

<p align="center">
  <img width="1392" height="659" alt="image" src="https://github.com/user-attachments/assets/5611bc28-c155-429e-8384-a9f9d26de2cd" />
</p>

**Problema:** Mensagens de erro genéricas sem orientação  
**Severidade:** 4 - Catastrófico  
**Descrição:** Erros como "Falha no upload" ou "Erro ao fazer login" não explicam o problema nem sugerem solução. Usuário fica sem direcionamento.

**Recomendação:**

Mensagem correta: **Arquivo Inválido**

Problema: O arquivo selecionado não é um modelo PyTorch válido (.pt)

Como resolver:
1. Verifique se o arquivo tem extensão .pt
2. Certifique-se de que o modelo foi exportado corretamente
3. Tente exportar novamente usando torch.save()

> **Observação:** Mensagens educativas transformam frustração em aprendizado.

---

### Heurística 10 – Ajuda e Documentação

<p align="center">
  <img width="1392" height="659" alt="image" src="https://github.com/user-attachments/assets/b75e67f0-0d5f-454c-a3f6-82251e2cf8ed" />
</p>

**Problema:** Ausência total de sistema de ajuda  
**Severidade:** 3 - Grave  
**Descrição:** Não há botão (?), link para documentação ou ajuda contextual em nenhuma tela. Usuários sem recurso oficial para dúvidas.

**Recomendação:**
- Ícone "?" fixo no canto superior direito
- Ajuda contextual por tela
- Documentação: Introdução, Tutoriais, FAQ, Glossário
- Vídeos tutoriais curtos
- Tour guiado para novos usuários

> **Observação:** A tela de configurações poderia ter tooltips explicativos ao lado de cada campo técnico.

---

## ✅ Boas Práticas Identificadas

### Exemplo – Heurística 4 (Consistência e Padrões)

<p align="center">
  <img width="1392" height="656" alt="image" src="https://github.com/user-attachments/assets/813e0560-dffc-4351-9574-a424b71773a3" />
  <img width="1391" height="657" alt="image" src="https://github.com/user-attachments/assets/fc9aaa59-596d-4eaa-8b5d-01b2b3d0823e" />
</p>

**Boa Prática:** Consistência nos formulários de Login e Cadastro  
**Descrição:** Campos de entrada (email, senha) seguem o mesmo padrão visual em ambas as telas. Labels posicionados consistentemente, mesmo tamanho e estilo.

**Por que é bom:** Mantém familiaridade do usuário ao navegar entre telas relacionadas. Não precisa "reaprender" como interagir.

---

### Exemplo – Heurística 8 (Projeto Minimalista e Estético)

<p align="center">
  <img width="1392" height="655" alt="image" src="https://github.com/user-attachments/assets/ce1fd3c2-1cfe-4d94-955b-166e887850f5" />
</p>

**Boa Prática:** Interface limpa na tela de login  
**Descrição:** Apenas elementos essenciais: logo, campos email/senha, botão de login e links para recuperação. Sem informações desnecessárias.

**Por que é bom:** Interface limpa reduz carga cognitiva. Usuário foca na tarefa principal (fazer login).

---

### Exemplo – Heurística 3 (Controle e Liberdade)

<p align="center">
  <img width="1392" height="658" alt="image" src="https://github.com/user-attachments/assets/e99fee26-56ff-4e6d-8076-0e09d66ef653" />
</p>

**Boa Prática:** Link "Já tem uma conta? Entrar" no cadastro  
**Descrição:** Saída clara do fluxo de cadastro, permitindo retorno ao login sem completar formulário.

**Por que é bom:** Oferece "saída de emergência" sem forçar conclusão de tarefa indesejada. Respeita autonomia do usuário.

---

## Resumo da Avaliação

### Problemas por Severidade

| Severidade | Quantidade | Prioridade |
|-----------|-----------|-----------|
| 4 - Catastrófico | 2 | 🔴 Corrigir IMEDIATAMENTE |
| 3 - Grave | 2 | 🟠 Alta prioridade |
| 2 - Simples | 2 | 🟡 Média prioridade |
| 1 - Cosmético | 0 | 🟢 Baixa prioridade |
| **TOTAL** | **6** | |

---

### Heurísticas Mais Violadas

1. **Heurística 5 - Prevenção de Erros** (Severidade 4)
2. **Heurística 9 - Reconhecer e Recuperar Erros** (Severidade 4)
3. **Heurística 3 - Controle e Liberdade** (Severidade 3)
4. **Heurística 10 - Ajuda e Documentação** (Severidade 3)

---

### Problemas Críticos (Severidade 4)

| # | Heurística | Problema | Tela Afetada |
|---|-----------|----------|--------------|
| 1 | H5 - Prevenção de Erros | Falta de validação de formato de arquivo (modelo .pt) | Configurações |
| 2 | H9 - Recuperar Erros | Mensagens de erro genéricas sem orientação | Múltiplas telas |

---

### Recomendações Prioritárias

#### Imediatas (Severidade 4)
- **Implementar validação robusta de arquivos .pt**
  - Restringir extensão no dialog do sistema
  - Validar assinatura do arquivo
  - Impedir salvamento com arquivo inválido
  
- **Criar sistema de mensagens de erro educativas**
  - Explicar o problema em linguagem clara
  - Sugerir passos concretos de solução
  - Incluir links para documentação/suporte

#### Alta Prioridade (Severidade 3)
- **Botão de cancelar análise**
  - Permitir interromper processamento
  - Confirmação antes de cancelar
  - Limpar resultados parciais
  
- **Sistema de ajuda contextual**
  - Ícone "?" em todas as telas
  - Tooltips explicativos
  - Tour guiado para novos usuários

#### Média Prioridade (Severidade 2)
- **Preview visual de relatórios**
  - Thumbnails de vídeos/imagens testadas
  - Tags visuais de status
  - Resumo de métricas principais
  
- **Filtros avançados**
  - Busca por múltiplos critérios
  - Salvar filtros favoritos
  - Atalhos para usuários experientes

---

## Conclusão

As avaliações foram realizadas sobre **protótipos desenvolvidos no Figma**, ainda em fase inicial de desenvolvimento.

A análise revelou que o sistema possui **boa base de design visual** (interface limpa, consistência nos formulários), mas apresenta **problemas críticos de usabilidade** que podem comprometer a experiência das três personas principais:

- **Paulo Andrade (Engenheiro de ML):** Precisa de validação de arquivos, controle sobre análises em andamento e filtros avançados para trabalho diário.
- **Ricardo Santos (Gerente de Segurança):** Necessita de mensagens de erro claras, ajuda contextual e preview visual de relatórios para decisões rápidas.
- **Fernanda Costa (Gestora de Projetos):** Requer interface simplificada com sistema de ajuda robusto para apresentações executivas.

### Insights Principais

**Pontos Fortes:**
- Design visual limpo e profissional
- Consistência em formulários de login/cadastro
- Boa hierarquia visual de informações
- Presença de "saídas de emergência" (link voltar ao login)

**Pontos Críticos:**
- **Ausência de validações essenciais** (risco de crashes e corrupção)
- **Mensagens de erro não-educativas** (deixa usuário sem direção)
- **Falta de controle durante processamento** (sem opção de cancelar)
- **Sem sistema de ajuda** (aumenta curva de aprendizado)

### Impacto nos Objetivos do Projeto

O projeto tem como meta **"reduzir tempo gasto em tarefas manuais e repetitivas"** e **"facilitar tomada de decisão"** (conforme documento de personas). Os problemas identificados impactam diretamente esses objetivos:

- Impossibilidade de cancelar análises causa perda de tempo
- Validações inadequadas causam erros evitáveis e retrabalho
- Ausência de ajuda prolonga curva de aprendizado
- Falta de filtros reduz eficiência de usuários experientes

### Alinhamento com as Personas

| Persona | Principal Necessidade | Violação Crítica Relacionada |
|---------|----------------------|------------------------------|
| **Paulo Andrade**<br>(Engenheiro de ML) | Agilidade e controle nos testes | H3: Impossibilidade de cancelar análise<br>H5: Validação de arquivos |
| **Ricardo Santos**<br>(Gerente de Segurança) | Compreensão clara de resultados e erros | H9: Mensagens de erro genéricas<br>H10: Falta de ajuda contextual |
| **Fernanda Costa**<br>(Gestora de Projetos) | Acesso rápido e intuitivo | H6: Dificuldade em reconhecer relatórios<br>H7: Ausência de filtros |

> **Próximos passos:** 
> 1. Priorizar correção dos **2 problemas catastróficos** antes do teste com usuários reais
> 2. Implementar sistema de ajuda contextual
> 3. Adicionar controle de processamento (cancelar/pausar)
> 4. Melhorar reconhecimento visual de relatórios
> 
> Com essas correções, o sistema estará pronto para validação com as personas reais.

---

**Avaliadores:** Lucas Dias, Samir Oliveira, Pedro Algodoal, Caio Conceição, Guilherme Couto   
**Método:** Avaliação Heurística (Nielsen, 1994)
