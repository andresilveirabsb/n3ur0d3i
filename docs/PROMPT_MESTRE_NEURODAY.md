# 📌 PROMPT MESTRE DEFINITIVO – NEURODAY

## (VERSÃO CONSOLIDADA, COMPLETA E OFICIAL PARA CODEX)

## 1️⃣ CONTEXTO DO PROJETO

Você está desenvolvendo o Neuroday, um Recurso Educacional Digital, objeto de uma pesquisa de mestrado, desenvolvido integralmente em Flutter (Dart).

O sistema é:
- Cientificamente fundamentado
- Arquiteturalmente robusto
- Escalável
- Seguro
- Modular
- Pronto para produção
- Metodologicamente justificável

Ele é voltado para:
- Organização visual
- Estruturação de rotinas
- Previsibilidade
- Reforço positivo
- Comunicação família–escola
- Desenvolvimento de autonomia

⚠️ Este sistema não é experimental.
É um instrumento acadêmico formal.

## 2️⃣ REGRA DE NEGÓCIO INEGOCIÁVEL

🚫 É PROIBIDO:
- Inventar funcionalidades
- Acrescentar melhorias não solicitadas
- Alterar regras pedagógicas
- Modificar fluxos
- Simplificar arquitetura
- Adicionar integrações não solicitadas
- Criar features extras
- Introduzir gamificação além da pontuação por moedas 🪙
- Implementar notificações push se não solicitado
- Criar IA interna
- Criar ranking

Se houver dúvida:
- Perguntar
- Não presumir
- Não improvisar

## 3️⃣ ARQUITETURA OBRIGATÓRIA

Clean Architecture

```text
lib/
  core/
  features/
    students/
    routines/
    tasks/
    timer/
    rewards/
    progress/
    chat/
    settings/
```

Cada feature deve conter:

```text
data/
domain/
presentation/
```

Domain:
- Entities
- Repository (abstract)
- UseCases

Data:
- Models
- DataSources
- RepositoryImpl

Presentation:
- Pages
- Widgets
- State management (Riverpod ou BLoC, conforme definido pelo usuário)

⚠️ Domain não depende de Flutter
⚠️ Presentation não acessa Firestore diretamente

## 4️⃣ PERFIS E CONTROLE DE ACESSO

### 👤 Modo Administrador (Responsável)
Pode:
- Criar e editar agenda
- Criar e editar tarefas
- Configurar contadores
- Configurar horários
- Integrar Google Calendar
- Integrar Google Tasks
- Criar recompensas
- Configurar moedas 🪙
- Personalizar temas, ícones, sons
- Upload de imagens e áudios

### 👦 Modo Usuário (Criança)
Pode apenas:
- Visualizar agenda
- Executar tarefas
- Incrementar contadores
- Iniciar cronômetro
- Ganhar moedas 🪙
- Solicitar resgate de recompensa

🚫 NÃO pode editar nada.

## 5️⃣ INTEGRAÇÃO OBRIGATÓRIA COM GOOGLE

A Agenda e as Tarefas devem estar vinculadas à conta Google do Administrador.

### Google Calendar
- Eventos criados no Neuroday devem refletir no Google Calendar
- Eventos do Google Calendar devem sincronizar com o Neuroday
- Edição somente no modo Administrador

### Google Tasks
- Tarefas criadas no Neuroday devem sincronizar com Google Tasks
- Tarefas do Google Tasks devem refletir no Neuroday
- Somente Administrador pode editar

⚠️ Modo Usuário executa apenas o que já foi configurado.

## 6️⃣ AGENDA VISUAL (CORE)

- Visualização diária
- Cards visuais
- Ordem cronológica
- Status (pendente/concluído)
- Integração Google Calendar
- Cache offline
- Stream reativo

## 7️⃣ TAREFAS E CONTADORES

### Tipo A – Contador Quantitativo
Exemplo:
- 3/8 copos de água

Administrador define:
- Total
- Unidade
- Pontuação 🪙

Usuário:
- Incrementa manualmente

Ao atingir total → ganha moedas

### Tipo B – Contador com Intervalo Temporal
Exemplo:
- 2/3 doses de medicamento

Administrador define:
- Total
- Intervalo (ex: 4h) OU horários fixos
- Bloqueio fora do horário

Sistema:
- Impede incremento fora do intervalo
- Pode iniciar cronômetro
- Pode disparar som

## 8️⃣ CRONÔMETRO VISUAL

- Contagem regressiva
- Pode estar vinculado a tarefa
- Dispara som ao zerar
- Registra timestamp

## 9️⃣ SISTEMA DE SOM

Administrador pode:
- Escolher som padrão
- OU
- Upload de áudio (mp3/wav)

Configurar:
- Volume (0–100%)
- Aplicação por evento

Fallback obrigatório para som padrão.

## 🔟 PERSONALIZAÇÃO (ACESSIBILIDADE TEA)

Configuração por estudante:
- Tema (claro, escuro, alto contraste)
- Cores personalizadas
- Fonte
- Tamanho da fonte
- Tamanho do ícone
- Cor do card
- Bordas
- Espaçamento

Persistência individual por estudante.
Aplicação dinâmica.

## 11️⃣ CARDS VISUAIS

Cada card pode usar:
- Ícone configurável
- OU
- Foto real (upload)

Se houver imagem:
- Substitui ícone
- Mantém proporção
- Otimização obrigatória

## 12️⃣ GAMIFICAÇÃO – SISTEMA DE MOEDAS 🪙

A única gamificação permitida é baseada em moedas 🪙.

Funcionamento:
- Cada tarefa concluída gera moedas
- Contadores geram moedas ao completar meta
- Moedas acumuladas por estudante

Administrador cadastra recompensas:
Exemplos:
- 120🪙 = 30 min extra de videogame 🎮
- 80🪙 = casquinha 🍦
- 155🪙 = McLanche 🍔

Regras:
- Não permitir resgate sem saldo suficiente
- Deduzir moedas corretamente
- Registrar histórico imutável
- Recompensas ativáveis/desativáveis

## 13️⃣ PROGRESSO E REGISTROS

- Registro textual
- Upload de imagem
- Timeline cronológica
- Permissão por vínculo

## 14️⃣ CHAT FAMÍLIA–ESCOLA

- Tempo real (Firestore stream)
- Restrito por vínculo
- Identificação do remetente
- Marcação de leitura

## 15️⃣ ENTIDADES IMPORTANTES (DOMAIN)

- Student
- Task
- TaskCounterConfig
- TaskScheduleConfig
- Reward
- CoinTransaction
- AudioConfig
- CardStyleConfig
- StudentAccessibilityConfig
- Routine
- CalendarEvent

⚠️ Configurações devem ser entidades separadas.

## 16️⃣ QUALIDADE TÉCNICA OBRIGATÓRIA

- Null safety
- Código compilável
- Sem pseudocódigo
- Sem comentários vagos
- Tratamento de exceções
- Validações explícitas
- Logs estruturados
- Arquivos completos

## 17️⃣ FLUXO OBRIGATÓRIO DO CODEX

Antes de gerar código:
- Confirmar entendimento
- Reafirmar que não adicionará funcionalidades
- Apresentar estrutura
- Somente então implementar

## 18️⃣ MISSÃO FINAL

Implementar exatamente o especificado:
- Com rigor acadêmico
- Excelência técnica
- Arquitetura limpa
- Escalabilidade
- Fidelidade científica
- Sem invenções
- Sem alterações não autorizadas
- Sem expansão de escopo
