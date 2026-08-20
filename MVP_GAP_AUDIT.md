# Auditoria de lacunas — MVP GAG Core / KIA

Data de auditoria: 18 de agosto de 2026.

## Escopo confirmado

O GAG Core permanece uma plataforma interna da GAG. Esta auditoria não autoriza clientes, dados de demonstração, integrações externas, WhatsApp, faturação, marketplace, white-label, CRM avançado ou automações autónomas.

## O que já funciona

| Área | Estado observado | Limite mantido |
|---|---|---|
| KIA | Chat com Core Knowledge, RAG de conhecimento carregado, deteção de idioma, tarefas preparadas e confirmação explícita | Não grava tarefas sem confirmação |
| Voz | Entrada e síntese nativas, preferência de voz e estados de interação | Não mantém escuta contínua nem executa ações sozinha |
| Knowledge Base | Conteúdo manual, carregamento de procedimentos, listagem e remoção | Não inventa factos externos |
| Tarefas | Criação, edição técnica, estados, prioridade e backlog persistente | Apenas o proprietário acede às rotas |
| Agent Factory | Quatro critérios persistentes, criação única em Rascunho, teste isolado e ativação com transições protegidas | Sem criação ou ativação automática |

## Lacunas reais a completar

| Prioridade | Lacuna observada | Resultado necessário no MVP |
|---|---|---|
| P0 | O contexto do chat é enviado pelo cliente e não sobrevive a atualização da página | Histórico persistente por proprietário, leitura controlada e opção explícita de limpar |
| P0 | A Knowledge Base permite criar e remover, mas não editar um item já guardado | Edição confirmada de título, categoria e conteúdo, sem alteração silenciosa |
| P0 | As tarefas guardam trimestre, mas não uma data de prazo estruturada; a interface não expõe edição nem transições rápidas | Prazo opcional, edição, filtros e transições explícitas de estado |
| P0 | O dashboard mostra contagens básicas, mas não consolida aprovação da KIA, estado de agentes e distribuição operacional de tarefas | Indicadores reais, calculados da base de dados, sem números fictícios |
| P0 | A Factory possui permissões em texto e um teste isolado, mas não declara nível de autonomia nem permissões estruturadas | Nível Assistido por defeito, permissões READ/CREATE/EDIT/DELETE/EXECUTE/SEND/PUBLISH e bloqueio de ações externas |
| P0 | Não existe manifesto, ícone ou registo de service worker | Preparação PWA básica e instalável quando o navegador suportar |

## Critério de conclusão técnica

O MVP desta fase estará pronto quando a KIA tiver memória persistente controlável, os dados operacionais puderem ser revistos sem edição silenciosa, a Agent Factory conservar o ciclo humano obrigatório e a aplicação disponibilizar uma instalação PWA básica. A criação do primeiro agente continuará a depender exclusivamente de requisitos reais fornecidos pelo proprietário.
