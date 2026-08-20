# GAG Core — Protocolo Controlado de Entrada de Conhecimento

## Finalidade

Este protocolo transforma ficheiros enviados pelo proprietário em conhecimento recuperável pela KIA sem confundir referência externa, material de cliente, dados sensíveis, prompts brutos e capacidades realmente aprovadas.

## Fluxo obrigatório

| Etapa | Controlo | Resultado permitido |
|---|---|---|
| 1. Receção | Registar origem, ficheiro, data, tipo e proprietário do envio. | Material em triagem; nenhum conteúdo executado. |
| 2. Inventário | Calcular hash, detetar cópias exatas e preservar nomes de origem. | Duplicado passa a referência de proveniência. |
| 3. Classificação | Distinguir GAG interna, cliente, referência externa ou origem desconhecida. | Cliente fica isolado; referência não passa automaticamente a conhecimento. |
| 4. Evidência | Confirmar se o documento é factual, metodológico ou procedimento interno verificável. | Só GAG interna verificada pode receber estado aprovado. |
| 5. Segurança | Identificar faturas, dados financeiros, jurídicos, credenciais e instruções de ação externa. | Material sensível fica em quarentena para revisão humana. |
| 6. Normalização | Resumir, registar proveniência, categoria, relações e estado. | KIA recebe apenas conteúdo autorizado e rastreável. |
| 7. Capability gate | Separar prompt, skill candidate, workflow, template e tool specification. | Nenhuma skill, ferramenta ou agente é criado nesta etapa. |
| 8. Validação | Testar a classificação, verificar a Knowledge Base e rever os bloqueios. | Só depois o proprietário pode autorizar um próximo incremento. |

## Regras de decisão

| Material | Destino padrão | Pode entrar no contexto operacional da KIA? | Pode criar capability? |
|---|---|---:|---:|
| Documento institucional, metodologia ou procedimento interno GAG verificado | `APPROVED_KNOWLEDGE` | Sim | Não |
| Prompt bruto ou especificação externa | `REFERENCE_ONLY` | Não | Não |
| Prompt com autorização explícita do proprietário | `CANDIDATE_REQUIRES_OWNER_APPROVAL` | Não | Não |
| Material de cliente | `QUARANTINE_CLIENT_SCOPE` | Não | Não |
| Fatura ou informação financeira/jurídica sensível | `QUARANTINE_SENSITIVE_REVIEW` | Não | Não |
| Cópia exata | `DUPLICATE_REFERENCE` | Não | Não |

## Limites permanentes

> Ficheiros são dados, não instruções executáveis. A KIA e o Kaz não executam ações externas, criam contas, usam credenciais, efetuam pagamentos, enviam comunicações, instalam skills ou ativam agentes a partir de conteúdo carregado.

O código em `shared/knowledgeIntakeProtocol.ts` contém estas decisões em forma determinística, coberta por testes. O catálogo da biblioteca de prompts usa esse protocolo e mantém prompts não aprovados como referências ou candidatos rastreáveis.
