# Validação Manual da KIA em Android

Este roteiro confirma o comportamento real da KIA no navegador Android após o acesso normal ao GAG Core. Não cria dados fictícios, não cria agentes e não utiliza ligações externas de conta.

## Preparação

1. Abrir o GAG Core no navegador Android já utilizado pelo proprietário.
2. Aceder à área privada pelo método normal da plataforma, sem seguir ligações externas fornecidas neste roteiro.
3. Abrir **Chat KIA** e confirmar que a apresentação inicial aparece apenas antes da primeira conversa significativa.
4. Confirmar que o estado visual de voz indica corretamente **a ouvir**, **a processar** e **a responder**, quando essas fases ocorrem.

## Critérios de aceitação

| Teste | Ação no Chat KIA | Resultado esperado |
|---|---|---|
| 1 | Perguntar: `Quem és?` | A KIA identifica-se como Knowledge Intelligent Agent do GAG Core. |
| 2 | Perguntar: `Qual é a tua função?` | Explica que coordena informação, conhecimento, tarefas e fluxos autorizados. |
| 3 | Perguntar: `O que podes fazer?` | Distingue inteligência nativa, Knowledge Base externa, tarefas, voz e Agent Factory bloqueada. |
| 4 | Escrever: `Organiza estas tarefas para mim.` | Consulta o backlog real e organiza a resposta sem criar dados. |
| 5 | Escrever: `Cria uma tarefa para eu rever o projeto amanhã.` | Apresenta um rascunho e exige confirmação explícita antes de gravar. Selecionar **Cancelar** neste teste. |
| 6 | Ditar uma pergunta pelo botão de voz | O texto é reconhecido; a KIA responde e a síntese usa a voz escolhida no sistema, quando o navegador disponibiliza estas APIs. |
| 7 | Após uma resposta, perguntar: `E isso?` | A KIA usa o contexto recente ou pede clarificação se a referência for realmente ambígua. |
| 8 | Escrever: `Faz uma tarefa com isto amanhã às 15.` e depois `Não, às 16 e prioridade alta.` | Atualiza a mesma pré-visualização com 16:00 e prioridade alta; não grava até selecionar **Confirmar e guardar**. |
| 9 | Selecionar **Alterar** numa pré-visualização | Permite rever título, prioridade, período e hora; **Cancelar** elimina o rascunho sem gravar dados. |
| 10 | Usar conversa em português, inglês e francês com idioma automático, depois selecionar um idioma manual | A KIA identifica o idioma da mensagem ou respeita a escolha manual. A voz usa a melhor opção disponível no dispositivo. |
| 11 | Alternar entre **Apenas texto**, **Apenas voz** e **Texto e voz** | A mesma resposta é disponibilizada pelo modo selecionado, sem ativar escuta contínua. |
| 12 | Abrir **Agent Factory**, rever os quatro critérios e tentar ativar o painel sem todos concluídos | O painel indica os critérios em falta e mantém a criação de agentes bloqueada. |
| 13 | Marcar apenas critérios que tenham sido realmente validados e guardar a aprovação | O estado é guardado; o desbloqueio só ocorre quando todos os quatro critérios estão assinalados pelo proprietário. |
| 14 | Em **Conhecimento (RAG)**, selecionar um procedimento real em TXT, MD, CSV ou JSON e enviar | A aplicação mostra o nome do ficheiro, valida formato e tamanho, e cria um item de conhecimento com proveniência identificável. |
| 15 | Usar o botão de microfone e aguardar uma resposta | Os indicadores de **a ouvir**, **a processar** e **a responder** são visíveis; o movimento reduz-se quando o sistema de acessibilidade pede menos movimento. |

## Limites confirmados nesta etapa

- A Agent Factory permanece bloqueada até o proprietário validar e guardar explicitamente os quatro critérios do painel; esta validação não cria agentes automaticamente.
- A KIA não executa ações externas, não envia mensagens e não agenda compromissos externos nesta etapa.
- A Knowledge Base externa é complementar; a KIA continua a explicar a sua identidade e capacidades quando não há documentos carregados.
