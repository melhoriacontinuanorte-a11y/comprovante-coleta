# Comprovante de Coleta - Alterosa Pneus

Projeto PWA pronto para GitHub Pages.

## Publicar gratuitamente no GitHub Pages

1. Entre no GitHub e crie um repositório público, por exemplo:
   `comprovante-coleta`
2. Envie TODOS os arquivos desta pasta para a raiz do repositório:
   - index.html
   - manifest.webmanifest
   - sw.js
   - icon-192.png
   - icon-512.png
   - logo-alterosa.png
   - .nojekyll
3. No repositório, abra **Settings > Pages**.
4. Em **Build and deployment**, escolha:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/(root)**
5. Clique em **Save**.
6. Aguarde a publicação. O endereço normalmente será:
   `https://SEU-USUARIO.github.io/comprovante-coleta/`

## Instalar no tablet Android

1. Abra o endereço publicado no Google Chrome.
2. Quando o navegador liberar a instalação, o próprio sistema exibirá:
   **"Instalar o Comprovante de Coleta?"**
3. Toque em **INSTALAR AGORA**.
4. O app ficará disponível na tela inicial do tablet.

Também existe um botão **INSTALAR APP** dentro da página quando a instalação estiver disponível.

## Observação

A instalação PWA e o compartilhamento nativo precisam de HTTPS. O GitHub Pages fornece HTTPS.


## WhatsApp no Android

Ao tocar em **COMPARTILHAR**, a mensagem da coleta é copiada automaticamente. No WhatsApp, toque em **Adicione uma legenda...** e escolha **Colar** antes de enviar o PDF.


## Botão COPIAR TEXTO

Depois de gerar o comprovante, use **📋 COPIAR TEXTO** para copiar a mensagem breve da coleta. No WhatsApp, ao compartilhar o PDF, toque em **Adicione uma legenda...** e escolha **Colar**.


## V5 - correção para coletas grandes

- Corrigido deslocamento das colunas quando o serviço vinha como `RECAPE (`.
- O token vazio gerado pelo `(` agora é removido antes da leitura de Serviço/Fogo/Medida.
- CEP/Cidade/UF passam a ser lidos da área do cliente, e não da filial.
- PDF deixou de ser uma imagem alta cortada em páginas.
- A tabela agora é desenhada diretamente pelo jsPDF, com quebra de página controlada e cabeçalho repetido.
- Testado para suportar coletas com 60+ pneus sem corrupção na linha 50.


## V7 - assinatura no tablet

- Campo de assinatura em canvas.
- Assinatura vai para o preview e para o PDF.
- Botão para limpar assinatura.


## V8 - duas assinaturas com nomes digitados

- Assinatura do Cliente + Nome do Cliente digitado.
- Assinatura do Coletor + Nome do Coletor digitado.
- As duas assinaturas e nomes vão para o preview, PDF e comprovante final.


## V9 - assinatura em coluna

- As áreas de assinatura da tela ficaram uma abaixo da outra.
- Melhor uso no tablet para assinar com mais conforto.
- Altura do quadro de assinatura aumentada para 220px.


## V10 - ajuste no campo de nome

- Corrigido corte visual do texto digitado nos campos de nome.
- Altura, padding, tamanho da fonte e line-height ajustados.
- Melhor legibilidade no tablet e no computador.


## V11 - correção de assinatura esticando no tablet

- Corrigido seletor CSS dos dois canvases de assinatura.
- Removidos eventos touch duplicados; agora usa Pointer Events.
- Captura do dedo/caneta durante todo o traço.
- Ignora coordenadas fora do quadro para evitar riscos longos.
- Redimensionamento do Chrome no tablet não recria o canvas desnecessariamente.
- Canvas é recalculado somente depois que a área de assinatura está visível.
