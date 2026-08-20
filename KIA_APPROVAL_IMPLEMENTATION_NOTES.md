# Notas de implementação — aprovação KIA

- A aprovação persistente usa quatro critérios: texto, voz, contexto/confirmações e limites de segurança.
- A Agent Factory só é elegível para desbloqueio quando os quatro critérios forem confirmados pelo proprietário.
- O carregamento de procedimentos deve guardar a origem do ficheiro e enviar apenas conteúdo de texto aceite para a Knowledge Base.
- O feedback da voz deve comunicar os estados de escuta, processamento e resposta sem ativar escuta contínua.
- As rotas protegidas confirmadas são `getKiaApproval`, `updateKiaApproval` e `uploadKiaProcedure`; a criação de agentes continua condicionada a `agentFactoryUnlocked`.
- A interface existente concentra o formulário de conhecimento na aba Knowledge Base, o estado de voz no cabeçalho do chat e o bloqueio da Agent Factory na respetiva aba.
