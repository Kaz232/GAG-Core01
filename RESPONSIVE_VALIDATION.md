# Validação Visual — KIA Voice & Mobile First

## Verificações concluídas

| Viewport | Área observada | Resultado |
|---|---|---|
| 360 × 800 | Dashboard, cabeçalho, navegação horizontal e cartões | A página mantém margens proporcionais, cartões de uma coluna e texto legível. A navegação permanece num contentor horizontal sem expandir o corpo da página. |
| 375 × 812 | Dashboard, cabeçalho, navegação horizontal e cartões | O layout mantém o mesmo sistema visual, sem cortes visíveis nos cartões ou no cabeçalho. |
| 390 × 844 | Dashboard, cabeçalho, navegação horizontal e cartões | O cabeçalho e os cartões mantêm hierarquia e legibilidade; a lista de separadores continua horizontal e contida. |
| 412 × 915 | Dashboard, cabeçalho, navegação horizontal e cartões | A distribuição de espaço mantém-se estável, sem overflow horizontal do corpo da aplicação. |
| 768 × 1024 | Cabeçalho autenticado, navegação e grelha de cartões | O cabeçalho mantém informação do proprietário sem esmagar a navegação; os cartões transitam para duas colunas. |
| 1024 × 768 | Navegação completa e grelha de cartões | A grelha mantém duas colunas com espaçamento uniforme e a navegação horizontal acomoda todos os separadores no contentor próprio. |
| 1280 × 720 | Desktop, cabeçalho, navegação e indicadores | Os quatro indicadores usam a largura disponível com hierarquia equilibrada e a navegação apresenta todos os separadores. |
| 1440 × 900 | Desktop amplo, cabeçalho, navegação e indicadores | O contentor máximo mantém leitura confortável e os cartões preservam escala e espaçamento consistentes. |

## Limite da validação automática

O capturador de pré-visualização inicia no separador Dashboard e não disponibiliza interação de clique para abrir o Chat KIA. A validação automatizada cobre compilação e testes; a validação manual do painel de voz recolhível e do fluxo Chat KIA permanece descrita em `KIA_ANDROID_VALIDATION.md`.

## Consolidação Kia — verificações adicionais

| Viewport | Área observada | Resultado |
|---|---|---|
| 1280 × 720 | Dashboard após a consolidação Kia | Cabeçalho, navegação e cartões mantêm escala, contraste e alinhamento consistentes. |
| 390 × 844 | Dashboard móvel após a consolidação Kia | Cartões mantêm uma coluna legível; a navegação horizontal permanece contida sem overflow do corpo. |

As capturas não permitem acionar o separador Chat KIA. Os cenários de apresentação inicial, pronúncia “Kia”, confirmação e cancelamento são cobertos pela suite automatizada e pelo roteiro manual Android.

## Extensões operacionais — verificações de estabilidade

| Viewport | Área observada | Resultado |
|---|---|---|
| 1280 × 720 | Dashboard após reinício, migração e extensões operacionais | A pré-visualização respondeu após o reinício. Cabeçalho, navegação e indicadores permaneceram alinhados e legíveis. |
| 390 × 844 | Dashboard móvel após reinício, migração e extensões operacionais | A grelha mantém uma coluna, o cabeçalho permanece legível e a navegação horizontal fica contida no próprio contentor. |

O capturador continua limitado ao separador Dashboard. A validação manual do painel de aprovação, do carregamento de procedimentos e dos indicadores de voz permanece necessária no fluxo autenticado do proprietário.

## Fluxo controlado da Agent Factory — verificação de base

| Viewport | Área observada | Resultado |
|---|---|---|
| 1280 × 720 | Dashboard e navegação após o ciclo de rascunho, teste e ativação controlada | O cabeçalho, os sete separadores e os indicadores permanecem alinhados e legíveis; não foram observados erros de renderização no ecrã inicial. |
| 360 × 800 | Dashboard e navegação horizontal em Android compacto | Os cartões passam para uma coluna, o cabeçalho continua legível e a navegação mantém o scroll dentro do contentor, sem alargar o corpo da página. |

O capturador não permite abrir interativamente o Chat KIA ou a Agent Factory. A validação visual e funcional desses controlos deve ser concluída pelo proprietário autenticado através dos dez cenários em `KIA_AGENT_FACTORY_E2E_VALIDATION.md`; a compilação e os testes automatizados cobrem as regras de recolha, cancelamento e transição de estados.

## MVP PWA — verificações iniciais

| Viewport | Área observada | Resultado |
|---|---|---|
| 360 × 800 | Entrada sem sessão do capturador | A aplicação apresenta o estado de verificação de sessão sem erro de renderização. A captura não herdou a sessão autenticada do proprietário. |
| 375 × 812 | Dashboard autenticado na pré-visualização | Cabeçalho, cartões de indicadores e navegação horizontal mantêm uma coluna legível, contraste suficiente e sem overflow horizontal visível. |
| 390 × 844 | Dashboard PWA em mobile intermédio | A navegação horizontal permanece no seu contentor e os quatro indicadores mantêm cartões de uma coluna, sem cortes visíveis. |
| 412 × 915 | Dashboard PWA em mobile amplo | Cabeçalho, cartões e resumo operacional preservam contraste e alinhamento; a área de separadores é navegável por scroll horizontal. |
| 768 × 1024 | Dashboard PWA em tablet vertical | Cabeçalho autenticado, navegação e cartões permanecem legíveis; os indicadores passam para duas colunas sem esmagamento. |
| 1024 × 768 | Dashboard PWA em tablet horizontal | A grelha de indicadores mantém duas colunas e a navegação completa permanece contida no respetivo contentor horizontal. |
| 1280 × 720 | Dashboard PWA em desktop | A barra de navegação apresenta todos os módulos e os quatro indicadores usam a largura de forma equilibrada. |
| 1440 × 900 | Dashboard PWA em desktop amplo | O contentor máximo mantém leitura confortável, alinhamento estável e espaço operacional sem distorção dos cartões. |

O manifest, a cor de tema, o ícone e o registo do service worker foram acrescentados para instalação em produção. O service worker não interceta pedidos `/api/`, preservando autenticação e operações protegidas em rede.
