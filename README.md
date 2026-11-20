# Tubos de Cor

Jogo relaxante de classificar cores em tubos de ensaio, projetado especialmente para celular **Android** (instalável como **PWA** e jogável offline).

## Como jogar

Toque em um tubo para selecioná-lo e depois toque no tubo de destino.
Blocos da mesma cor no topo são movidos juntos.
O objetivo é deixar cada cor inteira em um único tubo.

- **Desfazer:** volta a última jogada (disponível 20 segundos depois de cada uso).
- **Tubo extra:** adiciona um tubo vazio ao nível atual (disponível a cada 15 minutos; é mantido se você reiniciar o nível).
- **Símbolos nas cores (`◆`):** botão no topo para exibir formas geométricas sobre as cores, facilitando a leitura.
- **Instalar (`📲 Instalar`):** aparece quando o navegador permite instalar o jogo direto na tela inicial do Android.

## Progressão

Os níveis são gerados de forma determinística a partir do número do nível, suportando milhões de níveis reproduzíveis com tamanho ergonômico de tubos para leitura e toque confortáveis:

- **Níveis 1 a 180:** progressão linear gradual de **3 a 8 cores** e capacidade (altura) dos tubos de **4 a 6 blocos**.
- **Níveis 181 em diante:** platô confortável com **8 cores e capacidade 6**, alternando com **níveis de respiro** mais leves a cada 10 níveis (`185`, `195`, `205`...).
- **Níveis de atenção (1 tubo vazio):** a partir do nível 16, cerca de 15% a 25% dos níveis (nunca dois seguidos) têm apenas **1 tubo vazio** em vez de 2, exigindo mais atenção no planejamento.
- **Níveis surpresa:** a cada 10 níveis (`10`, `20`, `30`...), apenas o topo fica inicialmente visível e as cores vão sendo reveladas conforme você joga.
- Todos os níveis passam por busca verificadora antes de serem entregues, garantindo 100% de solução.

## Modo de teste

- Segure o indicador **"Nível N"** por cerca de 1 segundo para abrir o seletor de nível.
- Ou abra o jogo com `?nivel=1834` no endereço (sem sobrescrever o progresso salvo).

## Publicar no GitHub Pages e instalar no Android

1. Crie um repositório no GitHub e envie todos os arquivos e a pasta `icons/` deste diretório.
2. Em **Settings → Pages**, escolha a branch principal e a pasta `/ (root)`.
3. No Android (Chrome), abra o endereço publicado e toque em **Instalar** (ou no menu **⋮ → Adicionar à tela inicial**) para jogar em tela cheia e sem internet.

## Arquivos

- `index.html`: interface responsiva, motor do jogo, áudio sintetizado e diálogos nativos.
- `manifest.webmanifest`: manifesto PWA para instalação no Android.
- `sw.js`: Service Worker para cache e funcionamento offline.
- `icons/`: ícones do aplicativo (`icon.svg`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`).
- `README.md`: este arquivo.
