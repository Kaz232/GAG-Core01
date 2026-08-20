# GAG Core — Catálogo de Engenharia da Biblioteca de Prompts

**Estado:** análise e normalização inicial concluídas; nenhuma skill, ferramenta, integração ou agente foi criado por este catálogo.

## 1. Método e rastreabilidade

Os ficheiros originais permanecem inalterados em `/home/ubuntu/upload`. Foi criado um inventário não destrutivo com formato, hash SHA-256, classificação preliminar e pré-visualização textual. O inventário completo está em `PROMPT_LIBRARY_INVENTORY_2026-08-19.tsv`; os hashes estão em `PROMPT_LIBRARY_HASHES_2026-08-19.tsv`; e as duplicações exatas estão em `PROMPT_LIBRARY_EXACT_DUPLICATES_2026-08-19.txt`.

> O catálogo não trata qualquer prompt de origem externa como facto da GAG, integração disponível ou autorização operacional. Um prompt é preservado como referência; uma capability só pode nascer após especificação, revisão e aprovação humana.

## 2. Resultado do inventário

| Métrica | Resultado |
|---|---:|
| Ficheiros candidatos analisados | 120 |
| Ficheiros únicos por hash | 93 |
| Ficheiros redundantes exatos | 27 |
| Grupos de duplicação exata | 21 |
| Ficheiros Markdown | 88 |
| Ficheiros PDF | 28 |
| Ficheiros DOCX | 4 |
| Ficheiros de imagem | 1 |

A classificação preliminar usa categorias não exclusivas, porque um manual pode conter workflow, conhecimento e templates ao mesmo tempo.

| Categoria preliminar | Entradas associadas |
|---|---:|
| Knowledge | 35 |
| Reference | 83 |
| Skill candidate | 16 |
| Template | 40 |
| Workflow | 35 |
| Tool specification | 14 |

As cópias idênticas foram marcadas como redundantes no catálogo, mas não foram apagadas. A consolidação usa uma fonte primária por grupo e mantém todas as variantes como `SOURCE_REFERENCES`.

## 3. Classificação normalizada

| Grupo de origem | Classificação principal | Decisão de utilização no GAG Core |
|---|---|---|
| Normas, modelos-mestre e Prompt Bible | Knowledge + Template + Skill candidate | Base metodológica para prompting estruturado; requer adaptação às regras da GAG antes de uma skill ficar pronta. |
| GAG Labs, aulas, manuais, avaliações e exercícios | Knowledge + Workflow + Template | Base de formação e referência pedagógica; não é automaticamente procedimento operacional. |
| Coleções gerais de prompts | Reference + Skill candidate | Fonte para descobrir padrões equivalentes; manter fora do contexto geral da KIA e recuperar apenas por necessidade. |
| Roteiros, prompts cinematográficos e vídeo | Template + Skill candidate | Candidatos para produção de vídeo, roteiro e QA; exigem briefing, direitos de material e revisão humana. |
| NotebookLM, Gemini, ChatGPT, Replit e Apps Script | Tool specification + Reference | Conhecimento sobre ferramentas externas; não representa integração disponível no GAG Core. |
| CRM, apps e análise de dados | Reference + Tool specification | Fontes de requisitos e padrões; não autorizam acesso a contas, dados ou automações. |
| Deteção de golpes, finanças, imobiliário e contratos | Reference only | Conteúdo potencialmente sensível; nunca será tratado como conselho profissional nem como automação decisória. |

## 4. Skills candidatas consolidadas

As entradas abaixo são **fichas de competência candidatas**, não skills instaladas. Foram agrupadas por processo, não por prompt individual.

| Nome candidato | Finalidade | Principais fontes | Estado | Motivo do estado |
|---|---|---|---|---|
| `gag-prompt-engineering` | Recolher contexto, estruturar instruções, identificar lacunas e produzir prompts auditáveis. | Norma Técnica, Prompt Bible, modelos-mestre, listas de prompts. | **Needs review** | Precisa de adaptar regras de origem às políticas internas da GAG e definir limites de uso. |
| `gag-knowledge-curation` | Transformar documentos em conhecimento classificado, com fonte, incertezas, ligação e aprovação. | Materiais NotebookLM, Prompt para Base de Conhecimento, norma técnica. | **Needs review** | Deve reutilizar o intake já existente e não pode importar sem validação de autoridade. |
| `gag-ai-agent-design` | Preparar uma especificação de agente com objetivo, entradas, limites, permissões, testes e aprovação. | Materiais Gemini Gems, prompting interativo, KIA/Agent Factory existentes. | **Needs review** | A Agent Factory da GAG exige confirmação humana e não usa prompts externos como autorização. |
| `gag-video-production` | Converter briefing aprovado em roteiro, prompt cinematográfico, lista de cenas e QA. | Guia de roteiros, Prompt Bible, roteiro viral, vídeo/NotebookLM. | **Needs review** | Precisa de inputs de marca, direitos, formato e aprovação de cada peça. |
| `gag-content-production` | Preparar conteúdos, variações e estruturas de copy a partir de briefing verificado. | Materiais de aulas de conteúdo, listas de prompts e roteiros. | **Needs review** | Não publica, não envia e não afirma dados de clientes sem fonte. |
| `gag-design-with-ai` | Preparar briefing de design, direção visual, referências e checklist de qualidade. | Aulas de design com IA, identidade GAG, materiais Canva. | **Needs review** | Não substitui a identidade aprovada nem gera um produto final sem revisão criativa. |
| `gag-workflow-automation` | Converter processo aprovado numa especificação de automação com entradas, logs, exceções e aprovações. | Gemini + Apps Script, curso de automação, materiais Replit. | **Reference only** | Depende de conectores e credenciais que não estão aprovados nem configurados. |
| `gag-crm-requirements` | Estruturar requisitos de CRM, dados mínimos, estados e relatórios. | Prompt CRM, exemplos de apps e processos internos. | **Needs review** | Não cria CRM externo nem processa dados de clientes sem arquitetura e consentimento. |
| `gag-data-analysis-brief` | Converter uma pergunta operacional em briefing de análise, fontes e saída verificável. | Prompts de análise de dados e materiais de formação. | **Needs review** | A análise deve declarar fonte, período, cobertura e limites. |
| `gag-security-screening` | Preparar checklist de sinais de fraude, links suspeitos e pedido de validação externa. | Prompt Detectar Golp, relatório interno de segurança. | **Reference only** | Não pode emitir diagnóstico jurídico/financeiro nem autorizar transações. |

## 5. Templates candidatos

| Template candidato | Variáveis mínimas | Uso seguro |
|---|---|---|
| Briefing universal | objetivo, público, marca, formato, canais, restrições, fontes | Alimenta produção, design, vídeo ou análise sem inventar contexto. |
| Especificação de skill | finalidade, entradas, contexto, processo, limites, ferramentas, saída, QA, aprovação, fontes | Converte um processo real numa proposta controlável. |
| Especificação de ferramenta | problema, dados, permissões, ações permitidas, ações bloqueadas, logs, exceções, aprovação | Distingue capacidade desejada de integração realmente disponível. |
| Roteiro audiovisual | mensagem, duração, idioma, cenas, personagem, continuidade, requisitos de marca, restrições | Gera rascunho, não produção nem publicação automática. |
| Relatório interno | período, fontes, factos, progresso, bloqueios, riscos, decisões, próximos passos | Gera rascunho com origem e lacunas explícitas. |
| Intake documental | origem, tipo, sensibilidade, estado de evidência, resumo, relação, revisão | Regista documentos sem alterar os originais. |

## 6. Workflows identificados

| Workflow | Sequência | Limite |
|---|---|---|
| Engenharia de prompts | objetivo → contexto → regras → prompt → teste → revisão | Não cria ferramenta, agente ou integração sozinho. |
| Produção de conteúdo | briefing → estratégia → copy → design → vídeo → QA → aprovação | Não publica nem contacta terceiros. |
| Curadoria de conhecimento | intake → classificação → deduplicação → síntese → proveniência → aprovação → recuperação seletiva | Apenas conteúdo aprovado entra no contexto operacional da KIA. |
| Desenho de agente | necessidade → skills candidatas → especificação → testes → aprovação → ativação | Mantém criação e ativação humanas. |
| Automação interna | processo validado → dados → permissões → exceções → teste isolado → aprovação | Sem conectores, credenciais ou ações externas não aprovadas. |

## 7. Especificações de ferramentas referenciadas

Os materiais mencionam ChatGPT, Gemini, NotebookLM, Canva, Replit e Apps Script. Essas menções foram registadas como **referências de ferramenta**, não como integrações do GAG Core. Para cada futura ferramenta será exigido: objetivo, proprietário da conta, dados tratados, permissão mínima, testes, logs, botão de confirmação e forma de desativação.

## 8. Relação com KIA, Kaz e Agent Factory

| Componente | Pode consultar | Limite |
|---|---|---|
| KIA | Catálogo de skills candidatas, metodologia aprovada e referências seletivas | Não coloca a biblioteca inteira no contexto; não instala skills nem cria agentes automaticamente. |
| Kaz | Apenas Knowledge e skills explicitamente autorizadas pelo proprietário | Mantém autonomia Assistido, permissões internas e bloqueio de ações externas. |
| Agent Factory | Fichas de skills aprovadas como matéria-prima para uma futura especificação | Não usa prompts brutos para criar ou ativar agentes. |

## 9. Prioridade recomendada

1. `gag-knowledge-curation` — reforça a base permanente e evita perda ou mistura de informação.
2. `gag-prompt-engineering` — normaliza a forma como a KIA e o Kaz trabalham com pedidos futuros.
3. `gag-data-analysis-brief` — torna relatórios e análises verificáveis antes de avançar para automações.
4. `gag-video-production` — aproveita os ativos de formação e produção sem permitir publicação autónoma.
5. `gag-content-production` — prepara a cadeia briefing → copy → QA para produção interna.
6. `gag-design-with-ai` — alinha produção visual às diretrizes de marca da GAG.
7. `gag-ai-agent-design` — apoia a Agent Factory sem reduzir as aprovações humanas.
8. `gag-crm-requirements` — organiza requisitos antes de ligar fontes de leads ou dados de clientes.
9. `gag-workflow-automation` — só depois de as integrações necessárias serem aprovadas e configuradas.
10. `gag-security-screening` — permanece referência preventiva, com revisão humana e sem decisões automáticas.

## 10. Próximo controlo humano necessário

O catálogo está pronto para servir de índice da KIA por recuperação seletiva. Antes de criar qualquer ficheiro de skill reutilizável, ferramenta técnica ou agente, o proprietário deve escolher a primeira capability candidata a detalhar. A recomendação é começar por `gag-knowledge-curation`, porque ela fortalece todas as entradas futuras sem ampliar permissões nem introduzir ações externas.
