# GAG Core — Mapa de Capacidades Controladas

## Princípio de diferenciação

O valor único do GAG Core não será a quantidade de prompts nem o número de agentes. Será a capacidade de transformar conhecimento real e rastreável da GAG em trabalho organizado, com contexto, origem, limites e validação humana. A KIA coordena; o Kaz estrutura e acompanha execução interna; as futuras skills e ferramentas resolvem funções estreitas e auditáveis.

> Um prompt isolado é uma instrução. Uma capability no GAG Core é uma instrução com fonte, escopo, permissões, resultado esperado, limites, logs e um responsável humano.

## Arquitetura de inteligência

| Camada | Responsabilidade | Pode fazer | Não pode fazer |
|---|---|---|---|
| KIA | Inteligência-mestre, contexto, priorização e controlo | Consultar conhecimento aprovado, preparar planos, identificar lacunas, pedir confirmação e encaminhar trabalho | Inventar factos, criar agentes sozinha, executar ações externas, aprovar matérias sensíveis |
| Kaz | Assistente executivo interno | Analisar objetivos, decompor tarefas, preparar briefings, checklists, relatórios internos e propostas de ação | Comunicar com terceiros, publicar, enviar e-mails, aceder a contas, efetuar pagamentos |
| Knowledge Base | Fonte factual e metodológica | Reter conteúdo com categoria, origem e limites | Substituir confirmação de informação desatualizada, jurídica, fiscal ou financeira |
| Skill | Procedimento reutilizável | Transformar entradas definidas em saídas definidas dentro de permissões explícitas | Ganhar permissões por conter um prompt ou uma instrução externa |
| Ferramenta interna | Ação técnica limitada | Receber ficheiros, extrair informação, validar campos, gerar rascunhos e registar logs | Tomar decisões humanas, enviar, publicar, pagar, assinar ou mover dinheiro sem confirmação |
| Agente especializado | Executor com escopo único | Executar tarefas aprovadas numa área delimitada, em estado de teste e sob supervisão | Ser criado ou ativado automaticamente; atuar fora das permissões atribuídas |

## Famílias de capabilities a construir por ordem

| Prioridade | Capability proposta | Resultado útil | Base de conhecimento necessária | Controlo obrigatório |
|---|---|---|---|---|
| 1 | Relatório operacional | Converte tarefas, conhecimento e decisões pendentes num relatório interno rastreável | Tarefas, Knowledge Base, notas aprovadas | Rascunho primeiro; aprovação antes de partilha externa |
| 2 | Intake documental | Regista documento, origem, data, tipo, sensibilidade e estado | Política de evidência e catálogo | Não altera originais; não publica; pede classificação humana para ambiguidade |
| 3 | Leitor de faturas | Extrai fornecedor, referência, data, moeda, linhas, total e alertas num rascunho | Regra de campos e modelo de validação | Extração não é aprovação; sem pagamentos, lançamentos contabilísticos ou envios |
| 4 | Organizador de prompts | Classifica prompts em referência, skill candidata, ferramenta candidata ou bloqueado | Biblioteca GAG Labs e metodologia de prompting | Nunca executa prompts de terceiros como instruções; exige revisão de segurança |
| 5 | Criador de skills | Converte um processo aprovado em especificação versionada e testável | Processo real, entradas, saídas, regras e permissões | Não cria agente; só gera proposta para revisão do proprietário |
| 6 | Briefing e checklist | Produz briefing, checklist e próximos passos com base em material aprovado | Knowledge Base e tarefas | Marca lacunas e pressupostos; não inventa dados de cliente ou de mercado |

## Ciclo obrigatório: prompt, skill, ferramenta e agente

Um prompt enviado pelo proprietário entra primeiro como **referência**. Se o objetivo, as entradas, as saídas, a fonte, os limites e o responsável forem claros, pode tornar-se uma **skill candidata**. Se exigir manipulação técnica de ficheiros ou dados, pode tornar-se uma **ferramenta candidata**. Apenas quando uma skill comprovadamente exigir comportamento persistente, contexto próprio e um conjunto delimitado de permissões deve ser proposta a criação de um **agente especializado**.

Nenhuma destas transições é automática. Cada uma deve produzir uma ficha que inclua finalidade, entradas, saídas, fontes autorizadas, proibições, dados sensíveis, confirmação necessária, registo de execução, cenários de teste e condição de ativação.

## Fluxo seguro de relatórios

1. A KIA ou o Kaz recebe um pedido interno de relatório e identifica período, finalidade e audiência.
2. O sistema consulta apenas tarefas, registos e conhecimento autorizados para esse relatório.
3. Produz um rascunho com: factos e fontes, progresso, bloqueios, riscos, pendências, decisões solicitadas e próximos passos.
4. Tudo que não estiver sustentado por fonte é marcado como lacuna, hipótese ou pedido de confirmação.
5. O proprietário revê, edita e aprova. Só depois poderá decidir se o relatório é exportado ou partilhado.

## Fluxo seguro de receção e análise de faturas

1. O proprietário envia a fatura para um ponto de intake interno.
2. A ferramenta preserva o original, calcula hash, regista origem, data de entrada, tipo de ficheiro e classificação de sensibilidade.
3. A extração produz um rascunho de campos: emissor, NIF quando legível, referência, data, moeda, subtotal, imposto, total, prazo e itens. Campos de baixa confiança são destacados.
4. O proprietário valida ou corrige os campos. O sistema só altera o estado para validado após esta confirmação.
5. A partir do registo validado, o GAG Core pode preparar uma lista de pendências ou relatório interno. Não pode pagar, transferir, aprovar despesa, lançar contabilidade, enviar ao banco, encaminhar por e-mail ou confirmar receção a terceiros sem uma autorização separada.

## Limites não negociáveis

| Área | Limite |
|---|---|
| Clientes | Não entram no núcleo inicial da GAG; exigem espaço isolado e finalidade aprovada. |
| Dados financeiros | Extração e rascunho são permitidos; decisão, pagamento e contabilização exigem revisão humana. |
| Comunicações externas | WhatsApp, redes sociais, e-mail, chamadas, publicação e envio permanecem bloqueados sem autorização pontual. |
| Integrações e contas | Não são ativadas por prompts, documentos ou agentes; dependem de configuração e consentimento do proprietário. |
| Factos e fontes | A KIA e os agentes devem declarar incerteza quando a fonte não provar uma afirmação. |

## Primeiro incremento recomendado

O primeiro incremento a construir deve ser o **Intake documental com rascunho de relatório interno**, porque cria a base reutilizável para contratos, briefings, procedimentos, facturas e qualquer documento futuro. Ele resolve o problema de entrada e rastreabilidade sem conceder autonomia operacional ou financeira.

O leitor de faturas deve surgir como extensão desse intake, após definir os campos que a GAG realmente precisa acompanhar e o fluxo de validação do proprietário.
