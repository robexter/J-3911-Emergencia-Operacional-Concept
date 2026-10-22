# U-39 — Falha simultânea da J-3911A/B | Análise técnica do procedimento

**Edição:** Concept V1.0, 22/10/2026. **Base documental:** imagem original do procedimento de 13 ações enviada para análise; Manual da Unidade 39, seção 8.7.2.1 (páginas 51–52), seção de integração de vapor (página 90), quadro de controle (página 136), descrições complementares (páginas 55, 56, 58, 59, 61 e 144).

## 1. Situação iniciadora

A bomba de borra J-3911B para e não retorna. A J-3911A, como reserva, não assume a função de circulação. É possível que o problema seja simultaneamente de equipamento e de circulação útil; comprovação de motor ligado não equivale a comprovação de vazão. A perda da bomba afeta uma das correntes essenciais para lavar as chicanas, recuperar calor e sub-resfriar o fundo da fracionadora E-3901.

O Manual informa que a borra é escoada do fundo da E-3901, via linha 39-192, à J-3911A/B. Parte vai a reciclo ao reator; outra parte passa por C-3904/C-3907 e, em seguida, C-3933, retornando acima da chicana B-1 via FIC-39162 e abaixo da chicana via FIC-39163. Uma terceira corrente, após C-3933, abastece a sucção da J-3912, bomba de óleo decantado. O sub-resfriamento de fundo reduz risco de coque associado a alta temperatura e elevado tempo de residência.

## 2. Cadeia causal da emergência

**Perda do circuito J-3911 → menor vazão de borra nos refluxos → redução simultânea da lavagem gás–líquido e da remoção de energia → potencial aumento de TIC-39186 e TIC-39180 → menor renovação/homogeneização do inventário pesado → risco de coqueamento, arraste de finos e deterioração do balanço térmico.**

As temperaturas não têm de subir à mesma velocidade. A zona de flash responde à energia do efluente vindo do conversor e ao contato com o refluxo superior, enquanto a temperatura de fundo depende do inventário pesado, dos retornos inferiores e do tempo de residência. A direção e taxa de variação do nível do fundo não podem ser previstas somente pela parada da bomba: dependem do balanço entre líquidos condensados, saídas por outras rotas e vaporização.

### Critérios térmicos

| Variável | Faixa registrada no Manual U-39 | Critério registrado na fotografia |
|---|---:|---:|
| TIC-39186, zona de flash | 330–420 °C | 440 °C por 5 min |
| TIC-39180, fundo E-3901 | 320–365 °C | 370 °C por 7 min |

A fotografia informa PV da TIC-39186 como média de TI-39186A/B/C/D/E. Uma média de cinco temperaturas pode mascarar um ponto individualmente mais quente. Os tempos são critérios citados pela fonte, não uma autorização para aguardar o esgotamento dessa exposição. Não há evidência nesta documentação de que sejam necessariamente temporizadores implementados como trip no DCS; essa informação deve ser conferida na matriz de causa e efeito.

## 3. Interpretação das 13 ações documentais

### 01 · TIC-39186 e HV-39157

Vigiar a temperatura na zona de flash, as leituras individuais dos cinco termopares, a vazão dos refluxos e a existência de perda funcional J-3911. O procedimento determina tentar segurar a temperatura pelo refluxo de carga via HV-39157 e considerar o nível do fundo. A ação busca remoção temporária de energia por um caminho alternativo. Não há dados para assegurar a capacidade da HV, sua fonte de alimentação, sua temperatura ou a localização física do retorno. Sua abertura não prova resfriamento.

### 02 · TIC-39180

Monitorar o fundo simultaneamente. Sem FIC-39163 efetivo, há menor sub-resfriamento e homogeneização do líquido; a exposição a alta temperatura pode favorecer coqueamento e obstruções. O nível LIC-39152, a tendência de temperatura e o inventário precisam ser reconciliados.

### 03 · J-3903A/B

A foto determina parar as bombas de carga se a J-3911 não for recuperada e os critérios térmicos se aproximarem. A finalidade é retirar a alimentação de hidrocarbonetos que gera vapores quentes no conversor e, consequentemente, reduzir a energia que alcança a fracionadora. A transição altera as condições do riser e dos dispersores, portanto exige coordenação com os intertravamentos e procedimentos específicos.

### 04 · Trip parcial, L-3901/L-3902 e J-3902

A interrupção da carga envolve a transição do conversor para uma condição de trip parcial, fechamento de slide valves conforme a lógica, parada do compressor de gás úmido e bloqueio de seus vapores. Os efeitos de pressão diferencial, inventário catalítico e selagem devem ser verificados. Comando de fechamento de válvula não substitui confirmação da posição real.

### 05 · Rota de gás de combustão

O desvio do gás do D-3904 que iria à GV-3901 para a chaminé muda as resistências de escoamento do sistema de combustão. A pressão do regenerador, a posição real dos equipamentos e os caminhos de bypass/recuperação devem acompanhar a decisão.

### 06 · GV-3901 e vapor dos catcoolers

O procedimento solicita manter a GV-3901 acesa e desviar vapor dos catcoolers à atmosfera. O Manual da U-39 descreve a rota de desvio de vapor dos catcoolers via PIC-39936 e silenciador SL-3917 quando a caldeira sai de operação. A configuração particular citada na fotografia exige validar condições de chama, água de alimentação, permissivos, tambor, temperatura e pressão. A manutenção de chama não autoriza ignorar proteção de caldeira.

### 07 · Ar para catcoolers e J-3901

Fechar as entradas de ar indicadas e parar o soprador segundo sequência aprovada significa adaptar a regeneração à indisponibilidade da conversão. Estado do J-3901, pressão de regenerador, ar residual e calor remanescente precisam de acompanhamento.

### 08 · Catalisador retificador → regenerador

O objetivo provável é diminuir inventário de catalisador no retificador antes da configuração final da parada. Entretanto, a fotografia lista a transferência após o fechamento das L-3901/L-3902, criando aparente dependência hidráulica a esclarecer. Somente a matriz de causa e efeito e o procedimento vigente permitem confirmar momento e viabilidade dessa transferência.

### 09 · Bicos de carga

Fechar o lado óleo dos bicos de carga impede alimentação indevida de óleo ao riser. A sequência com vapor de dispersão e purgas, a retenção de óleo em linhas quentes e a disponibilidade de utilidades devem seguir instruções próprias, para mitigar obstruções e coque.

### 10 · J-3910 / J-3906

O Manual identifica J-3910 como bomba de HCO e J-3906 como bomba de refluxo de nafta pesada. Com a fracionadora saindo de operação, os respectivos refluxos e inventários devem ser retirados em coordenação, sem antecipar desnecessariamente a perda de funções térmicas remanescentes.

### 11 · Bloqueios no limite de bateria

Bloquear saída de gasolina e GLP impede transferência de produtos que já não têm produção e especificação normais. Exige controle de pressões, inventário, destino e comunicação com unidades receptoras.

### 12 · Pumpout leve, E-3908/09/10

A orientação é manter alinhado o pumpout leve pelo LB oeste e retirar as colunas E-3908/09/10, respeitando os procedimentos de redução de carga, aquecimento, refluxo e níveis. Deve ser confirmada a capacidade de recebimento da rota de esgotamento.

### 13 · J-3905 via J-3919

A fotografia indica desviar a J-3905 para pumpout leve via J-3919. O Manual associa J-3905 à transferência do líquido do tambor de topo da E-3901, utilizado na absorção primária, e J-3919 ao reciclo de gasolina da desbutanizadora para a E-3904. A ligação de pumpout deve ser verificada no P&ID, com especial atenção a destino, pressão, isolamento e prevenção de retorno.

## 4. Pontos que requerem checagem documental

1. Confirmar revisão do procedimento da fotografia e sequência autorizada de transferência de catalisador e fechamento das slide valves.
2. Confirmar se tempos 5 e 7 minutos são indicadores procedimentais, alarmes temporizados ou atuações instrumentadas.
3. Validar fonte, destino, vazão e capacidade térmica da HV-39157 e sua influência sobre o nível de fundo.
4. Conferir processamento dos cinco termopares e possibilidade de rejeição de um sinal defeituoso.
5. Conferir bloqueio de vapores do J-3902, que está apenas referenciado na fotografia.
6. Validar configuração segura da GV-3901 e dos catcoolers em desvio do gás de combustão.
7. Confirmar FIC-39163 no P&ID: a descrição do Manual (p. 52) o posiciona como retorno inferior, embora quadro p. 136 o chame de superior.
8. Rever procedimentos associados a J-3910, J-3906, J-3905, J-3919, E-3908/09/10 e condições de pumpout.

## 5. Alcance da Concept

A Concept contém modelos de tendência empíricos e simplificados destinados a demonstrar *relações qualitativas*. Não reproduz equações de balanço da planta calibradas, parâmetros reais de troca térmica, níveis de disparo de instrumentação, condição de inventário, matriz de intertravamento ou tempos reais de resposta. As simulações não podem fundamentar decisões reais de operação.
