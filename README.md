# J-3911 — Emergência Operacional Concept V2.3

Página única interativa e PWA para estudo da falha de circulação de borra das J-3911A/B da U-39. Base documental: fotografia com 13 ações de emergência e Manual da U-39 (páginas 51–52, 90 e 136).

## Como publicar no GitHub Pages

1. Extraia **todo** o conteúdo deste pacote na raiz de um repositório (index.html, app.js, styles.css, sw.js, manifest.webmanifest, assets/).
2. No repositório GitHub, em **Settings → Pages**, selecione **Deploy from a branch**, branch `main` e pasta `/ (root)`.
3. Abra o endereço HTTPS publicado e recarregue caso uma versão antiga permaneça em cache. No dispositivo móvel, use **Instalar App** quando disponível ou a opção **Adicionar à tela inicial** do navegador.
4. O modo offline funciona após uma visita online e a instalação do service worker; testar o funcionamento em um navegador compatível.

## V2.3 — Novidades

- Comparação entre os cinco TI-39186 com injeção individual de desvio e leitura da PV média.
- Falha hidráulica fictícia em bomba acionada, com vazões dos dois retornos exibidas.
- Dois gráficos com escalas individuais, modo passo a passo e evolução das temperaturas.
- Quatro cenários CIC encadeados e avaliação com dezoito questões, ordem das letras equilibrada.
- Controle de ajuste do fluxograma em telas pequenas e navegação acessível pelos pontos de explicação.

## Critérios de projeto

Preservar as treze ações originais da fotografia, sem transformá-las em autorização de comando operacional. A simulação é deliberadamente ilustrativa, não possui correlação de dados da planta e não substitui P&IDs, matriz causa-efeito ou procedimentos aprovados. Confira CHANGELOG_V2.md e ANALISE_TECNICA.md.

## Correção V2.2 — LIC-39152

A versão V2.0 somava +0,42 p.p./min ao nível em carga. A V2.2 adota o mecanismo de queda observado na U-39 após perda dos refluxos superior/inferior de borra. O balanço de massa ilustra a redução da condensação nas chicanas e o aumento da vaporização do inventário de fundo; após retirada da carga a queda se atenua. Taxas arbitrárias, sem dados de planta.


## V2.3 — Contenção térmica e preservação provisória do inventário

- A taxa de queda do LIC-39152 foi reduzida em relação à V2.2. **Não foi inserido limite inferior artificial de nível**: a redução da quantidade de líquido disponível diminui a perda ilustrativa, mas não assegura margem operacional real.
- HV-39157 com comando gradual e resposta térmica atrasada na simulação; sua função primária é moderar as temperaturas TIC-39186/39180. Efeito sobre o nível ocorre indiretamente (menor vaporização/maior condensação), não como reposição de inventário contabilizada automaticamente.
- J-3912 com opção simulada de parada, FV-39164B com abertura graduável e LV-39152 com abertura graduável. A retirada é representada como **uma única vazão residual hipotética**, limitada pelos controles, sem somar artificialmente fluxos de saída.
- Caixa **“Há vazão residual disponível?”** permite testar o caso de ausência de alimentação efetiva à J-3912 quando a J-3911 estiver parada. Nesse caso, comandos J-3912/FV/LV deixam de influenciar o nível do modelo.
- Adicionado Caso D de treinamento CIC, com quatro decisões sobre correlação nível-temperaturas e dependência hidráulica. Avaliação ampliada para 18 questões com alternativas embaralhadas.
- As 13 ações originais continuam intactas. A redução da queda do nível não implica retomada segura da carga nem substitui a matriz de causa e efeito.

**Dependência em aberto:** confirmar em P&ID a posição e a relação da LV-39152 com a FV-39164B, os caminhos de retirada, as permissivas de J-3912 e a possibilidade real de fluxo residual após a perda de J-3911A/B. Não executar manobras reais com base no aplicativo.
