# J-3911 — Emergência Operacional Concept V2.2

Página única interativa e PWA para estudo da falha de circulação de borra das J-3911A/B da U-39. Base documental: fotografia com 13 ações de emergência e Manual da U-39 (páginas 51–52, 90 e 136).

## Como publicar no GitHub Pages

1. Extraia **todo** o conteúdo deste pacote na raiz de um repositório (index.html, app.js, styles.css, sw.js, manifest.webmanifest, assets/).
2. No repositório GitHub, em **Settings → Pages**, selecione **Deploy from a branch**, branch `main` e pasta `/ (root)`.
3. Abra o endereço HTTPS publicado e recarregue caso uma versão antiga permaneça em cache. No dispositivo móvel, use **Instalar App** quando disponível ou a opção **Adicionar à tela inicial** do navegador.
4. O modo offline funciona após uma visita online e a instalação do service worker; testar o funcionamento em um navegador compatível.

## V2.2 — Novidades

- Comparação entre os cinco TI-39186 com injeção individual de desvio e leitura da PV média.
- Falha hidráulica fictícia em bomba acionada, com vazões dos dois retornos exibidas.
- Dois gráficos com escalas individuais, modo passo a passo e evolução das temperaturas.
- Três cenários CIC encadeados e avaliação com dezesseis questões, ordem das letras equilibrada.
- Controle de ajuste do fluxograma em telas pequenas e navegação acessível pelos pontos de explicação.

## Critérios de projeto

Preservar as treze ações originais da fotografia, sem transformá-las em autorização de comando operacional. A simulação é deliberadamente ilustrativa, não possui correlação de dados da planta e não substitui P&IDs, matriz causa-efeito ou procedimentos aprovados. Confira CHANGELOG_V2.md e ANALISE_TECNICA.md.

## Correção V2.2 — LIC-39152

A versão V2.0 somava +0,42 p.p./min ao nível em carga. A V2.2 adota o mecanismo de queda observado na U-39 após perda dos refluxos superior/inferior de borra. O balanço de massa ilustra a redução da condensação nas chicanas e o aumento da vaporização do inventário de fundo; após retirada da carga a queda se atenua. Taxas arbitrárias, sem dados de planta.
