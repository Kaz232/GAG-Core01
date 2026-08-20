# GAG Core + KIA — Plano de Execução do MVP

## Direção do produto

O **GAG Core** é a plataforma interna de operação. A **KIA — Knowledge Intelligent Agent** é o agente-mestre que interpreta conhecimento autorizado, mantém o contexto de trabalho, prepara ações e exige confirmação antes de qualquer alteração persistente. A Agent Factory existe como camada preparada para uma fase posterior: só poderá preparar agentes especializados depois de os critérios de aprovação serem validados explicitamente pelo proprietário.

> O MVP não pretende automatizar tudo. O seu objetivo é provar que o núcleo operacional funciona de forma segura, utilizável e testável.

## Escopo do MVP

| Prioridade | Resultado verificável | Estado atual |
|---|---|---|
| P0 | Autenticação e acesso exclusivo do proprietário | Implementado |
| P0 | Chat KIA com Core Knowledge e Knowledge Base separados | Implementado |
| P0 | Conversa natural, contexto temporário, confirmação, alteração e cancelamento de tarefas | Implementado e em validação contínua |
| P0 | Backlog e tarefas com dados reais do proprietário | Implementado |
| P0 | Voz por APIs nativas, sem escuta contínua por defeito | Implementado |
| P0 | Critérios visuais de aprovação antes de desbloquear a Agent Factory | Em implementação |
| P0 | Inclusão guiada de procedimentos reais na Knowledge Base com origem rastreável | Em implementação |
| P0 | Feedback de escuta e processamento da voz | Em implementação |
| P1 | Testes de fluxos essenciais, responsividade e registo de validação Android | Em execução |

## Limites explícitos do MVP

O MVP não cria clientes automaticamente, não cria agentes especializados por iniciativa própria, não executa automações externas e não inventa dados operacionais. A KIA pode preparar uma ação ou um rascunho apenas quando o proprietário o solicitar; qualquer gravação exige confirmação explícita. Espaços de clientes, agentes especializados ativos, integrações externas e automações recorrentes pertencem a fases futuras e exigem autorização específica.

## Critérios de aceitação do núcleo

| Fluxo | Critério de aceitação |
|---|---|
| Conhecimento | A KIA usa Core Knowledge nativo e conhecimento externo carregado de forma distinta, sem apresentar conteúdo não autorizado como facto. |
| Procedimentos | O proprietário pode inserir conteúdo ou carregar um procedimento em formato suportado; o registo mantém título, categoria e origem. |
| Tarefas | A KIA entende um pedido em linguagem natural, apresenta um resumo editável e só grava depois de confirmação explícita. |
| Voz | O utilizador vê se a KIA está a escutar, a processar ou a falar; o modo de escuta não inicia automaticamente. |
| Aprovação | A Agent Factory permanece bloqueada até que todos os critérios visuais sejam validados pelo proprietário. |
| Permissões | Todas as operações sensíveis permanecem protegidas por sessão e pelo papel de proprietário. |

## Sequência de entrega

O alvo de duas semanas corresponde a uma **meta de MVP**, não a uma garantia de prazo. A primeira semana concentra-se no núcleo que já está em curso: aprovação controlada, carregamento de procedimentos e feedback de voz. A segunda semana concentra-se em testes dos percursos completos, correções de estabilidade e validação manual em Android.

O objetivo de um mês para uma primeira versão comercial depende de a validação do MVP confirmar segurança, clareza de uso e consistência dos dados. Só depois disso devem ser planeadas funcionalidades de comercialização, configurações por organização, espaços de clientes e a criação controlada de agentes especializados.

## Próxima entrega técnica

A próxima entrega conclui o painel de critérios de aprovação, o carregamento rastreável de procedimentos reais e o feedback visual de voz. A entrega será aceite apenas com migração de base de dados não destrutiva, testes automatizados, validação visual em telemóvel e desktop, e checkpoint restaurável.
