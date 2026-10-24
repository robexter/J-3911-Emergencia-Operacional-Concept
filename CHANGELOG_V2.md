# J-3911 Emergência Concept V2.0 — Refinamentos

- Preservado integralmente o texto das 13 ações do documento original e análise técnica da V1.
- Novo painel dos cinco TI-39186 com cálculo da PV média, máximo, amplitude e injeção independente de desvio instrumental.
- Simulação de bomba acionada com vazão de borra indisponível e leituras simuladas de FIC-39162/63.
- Tendência reconstruída com dois painéis/eixos próprios e linhas de referência independentes.
- Avanço manual em passos de 15 segundos e atualização de temporizadores de exposição.
- 16 questões novas com alternativas próximas e embaralhamento Fisher-Yates.
- Cenários CIC agora propagam o histórico de decisões incorretas no texto e na telemetria das etapas seguintes.
- Fluxograma com botão de ajuste à tela; hotspots com navegação por teclado.
- PWA com cache V2 e instruções de fontes, incluindo limites do modelo didático.
- A V1 permanece preservada em diretório separado.

**Limites:** parâmetros dinâmicos, vazões relativas e desvios artificiais não representam calibração real. Os critérios 440°C/5 min e 370°C/7 min têm origem na fotografia; matriz de intertravamentos e capacidade da HV-39157 ainda requerem documentação atualizada para validação operacional.

## V2.1 — Correção da tendência do nível LIC-39152
- Retirada a regra fixa `dNível = +0,42 p.p./min` com carga e sem pumpout.
- Balanço explícito entre condensação, acréscimo hipotético via HV, vaporização e retiradas efetivas.
- Recirculação pela J-3911 não foi representada como perda líquida unilateral: retirada e retorno se cancelam.
- Com indisponibilidade de J-3911, a derivação para a sucção de J-3912 não é contabilizada como retirada normal.
- Três hipóteses selecionáveis: tendência de queda, elevação ou quase equilíbrio. Nenhuma afirma prever o LIC-39152 real.
- Gráfico dedicado de nível e indicadores de entradas, saídas e saldo em pontos percentuais por minuto (valores arbitrários).
- Revisão do texto de balanço de massa, atualização de versão e service worker para desatualização de cache.

## V2.2 — Revisão baseada no comportamento operacional da U-39
- Corrigida a direção de LIC-39152: perda simultânea dos refluxos superiores/inferiores produz queda rápida como condição-base do simulador da U-39.
- Retirados os cenários de elevação/equilíbrio de nível deste evento específico.
- Reorganizado balanço didático para explicar menos condensação dos pesados nas chicanas, mais vapor ascendente e vaporização do fundo.
- Controles existentes de HV-39157, parada de carga e pumpout afetam a tendência com parâmetros ilustrativos.
- Corrigidos os cenários CIC que mostravam LIC-39152 em elevação e revisadas opções/feedback.
- As 13 ações do procedimento original permanecem integrais.


## V2.3 — 23/10/2026 · Refinamento baseado no comentário operacional

1. Nível não despenca de forma tão rápida: reequilibrado o balanço ilustrativo do inventário, com perda progressivamente menor quando resta menos líquido disponível.
2. HV-39157 atua com atraso e reduz prioritariamente o avanço das temperaturas de flash e fundo; efeito secundário na perda por vaporização, sem injeção de massa presumida.
3. Controles independentes para ação simulada na J-3912, FV-39164B e LV-39152, condicionados à existência de retirada residual efetiva pela rota do produto.
4. Chave de hipótese hidráulica disponível para demonstrar ausência de efeito das ações quando não há vazão para retirar.
5. Exibido saldo de entradas/saídas e tendência de nível após cada intervenção, sem declarar recuperação nem criar um valor mínimo seguro fictício.
6. Cenário D com decisões encadeadas; avaliação aumentada para 18 perguntas.
7. V2.2 preservada; atualizado identificador do cache da PWA e responsividade dos novos controles mobile.

**Não validado:** abertura de LV-39152 / FV-39164B e dependência com J-3912; resposta real HV-39157; taxas numéricas de nível/temperatura. Nenhuma dessas hipóteses é sequência operacional aprovada.
