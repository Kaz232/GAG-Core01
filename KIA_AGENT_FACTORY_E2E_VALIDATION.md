# Validação ponta a ponta — KIA e Agent Factory

Este roteiro verifica o ciclo controlado implementado no GAG Core. Deve ser executado pelo proprietário autenticado, com dados e instruções reais da GAG. Não use nomes de clientes, integrações externas ou dados fictícios.

| Cenário | Ação do proprietário | Resultado obrigatório |
|---|---|---|
| 1. Critérios incompletos | Abrir **Agent Factory** e deixar pelo menos um critério desmarcado. Pedir à KIA para criar um agente. | A KIA informa que a Factory está bloqueada; nenhum rascunho, agente ou ação é criado. |
| 2. Desbloqueio explícito | Só depois de validar no uso real texto, voz, contexto/confirmações e segurança, marcar os quatro critérios e confirmar. | O painel indica aptidão apenas para preparar rascunhos. Não existe ativação automática. |
| 3. Recolha guiada por texto | No Chat KIA, pedir para criar um agente e responder aos dez requisitos com informação real. | A KIA recolhe nome, objetivo, função, tarefas, conhecimento, ferramentas, permissões, limitações, critérios de sucesso e testes, sem preencher campos por suposição. |
| 4. Revisão e edição | Rever a especificação, alterar um campo e confirmar a criação. | Surge um único agente em **Rascunho**. Cancelar antes da confirmação não cria nada. |
| 5. Teste isolado | Iniciar teste e enviar perguntas realistas na área isolada. | O agente responde apenas com a especificação; não cria tarefas, não altera dados, não usa integrações externas e não afirma ações executadas. |
| 6. Voz controlada | Usar **Falar** durante a recolha e durante o teste isolado. | Há indicação visual de escuta/processamento/resposta; a transcrição é tratada como entrada e continua a exigir confirmação visual. |
| 7. Ativação em duas etapas | Em **Em Teste**, escolher **Aprovar e ativar** e depois **Confirmar ativação**. | Só o segundo clique, após teste, muda o estado para **Ativo**. O cancelamento mantém **Em Teste**. |
| 8. Rejeição | Em **Em Teste**, escolher **Rejeitar**. | O estado muda para **Rejeitado** e não apresenta opção de ativar. |
| 9. Limite do checkpoint | Tentar pedir uma segunda criação quando já existe um agente. | A KIA e o servidor bloqueiam a segunda criação e orientam para rever o agente existente. |
| 10. Mobile | Repetir os cenários 3, 5 e 7 em largura de 360 px. | Campos, controlos de voz, edição, cancelamento e confirmação permanecem acessíveis sem sobreposição. |

## Registo de validação real

Preencha apenas depois de executar cada cenário com procedimentos reais da GAG.

| Data | Cenário | Resultado observado | Decisão do proprietário |
|---|---|---|---|
|  |  |  |  |

## Estado confirmado neste checkpoint

Em 18 de agosto de 2026, o proprietário confirmou os quatro critérios persistentes da KIA: texto, voz, contexto/confirmações e segurança. A Agent Factory encontra-se desbloqueada apenas para **preparar um rascunho**. A consulta de estado confirmou que não há agentes especializados registados; por isso, nenhum agente foi criado, testado, rejeitado ou ativado automaticamente.
