# Brenda IDE v3 — Blue iPad Edition

## Novidades
- Identidade azul e logo próprio (`brenda-ide-logo.jpg`).
- Preview em tempo real para celular/tablet/desktop.
- Autosave, busca, formatação, copiar código, backup e atualização com backup.
- Integração opcional com GitHub: listar repositórios com permissão de push, navegar em pastas, abrir arquivos e commitar.
- Backup local automático antes de cada commit.
- Token fica somente em `sessionStorage`: fechar a aba encerra a sessão da IDE.

## Conectar ao GitHub com o mínimo de acesso
Crie um **fine-grained personal access token** no GitHub:
1. Restrinja o token somente ao repositório que deseja editar.
2. Em Repository permissions, dê **Contents: Read and write**.
3. Não conceda Administration, Actions ou outras permissões que a IDE não precisa.
4. Na Brenda IDE, toque em **GitHub**, cole o token e conecte.
5. Abra um arquivo do repositório, edite e toque em **Commitar**.

A IDE não grava o token no código nem no `localStorage`; ele permanece somente na sessão da aba. Para uma publicação pública ainda mais robusta, o próximo passo recomendado é trocar PAT por uma GitHub App/OAuth com backend.

## GitHub Pages
Envie todos os arquivos deste ZIP para um repositório e habilite Settings → Pages → Deploy from a branch → main / root.


## v3.3 Minimal iPad
- Interface mais limpa e plana.
- Barra lateral compacta com atalhos.
- Rodapé e safe area do iPad em azul escuro, sem faixa branca.
- Mantém GitHub, backup manual, preview e atualização.

## v3.7 Abas, ZIP e mais preview
- **Abas de verdade**: cada arquivo aberto (single file, GitHub ou de dentro de uma pasta) vira uma aba na parte de cima do editor. Dá pra ter vários arquivos abertos ao mesmo tempo, trocar entre eles sem perder o que foi editado em cada um, e fechar abas individualmente (fecha a última e a IDE já abre um arquivo novo em branco pra nunca ficar sem nada editável).
- **Baixar tudo em .zip**: botão "Baixar .zip" na barra de ferramentas e também dentro do explorador de arquivos. Se uma pasta foi importada, o zip sai com a mesma estrutura de pastas; se são só arquivos avulsos abertos, saem soltos na raiz do zip.
- **Preview muito mais esperto por tipo de arquivo**:
  - PHP: preview best-effort (tags `<?php ?>` são removidas e o HTML ao redor é mostrado, com um aviso de que PHP não roda no navegador).
  - JavaScript: preview vira um console — mostra os `console.log/warn/error` e erros de execução, sem precisar abrir o DevTools.
  - CSS: preview mostra uma página de exemplo (títulos, botão, lista, card, campo de texto) já estilizada com o seu CSS.
  - JSON: preview mostra formatado/colorido, com aviso claro se o JSON estiver inválido.
  - Markdown: preview renderiza o Markdown como HTML de verdade (títulos, negrito, itálico, listas, links, imagens, citação, código).
  - SVG: preview renderiza a imagem vetorial diretamente.
  - HTML continua com preview ao vivo completo, inclusive resolvendo os caminhos relativos quando uma pasta está aberta.
- Ícone do app trocado: era azul (destoava do resto), agora é o gradiente roxo→magenta→laranja com "</>" branco, igual ao logo do cabeçalho e ao ícone do PWA (192px/512px).
- Todos os ícones de botão (código, arquivos, buscar, configurações, sobre, tema, GitHub, atualizar, copiar, formatar, backup, commitar, tamanhos de preview, tela cheia) trocados de emoji/símbolos soltos para um conjunto de ícones SVG consistente (traço fino, monocromático), em vez da mistura de emojis coloridos com símbolos Unicode.
- Página de Configurações de verdade (⚙ na barra lateral): tema, tamanho da fonte do editor, tamanho da tabulação, quebra de linha, números de linha, fechamento automático de colchetes e destaque da linha atual — tudo salvo entre sessões.
- Abertura de **pasta completa** do projeto (📁 Pasta no cabeçalho, ou pelo explorador de arquivos ▢ na barra lateral): navega em árvore de pastas/arquivos e troca entre eles mantendo as edições de cada um na memória da sessão.
- Com uma pasta aberta, o **preview resolve os caminhos relativos de verdade**: `<link href="css/style.css">`, `<script src="js/app.js">`, `<img src="img/logo.png">` etc. — inclusive `url(...)` dentro do próprio CSS — passam a carregar os arquivos certos dentro da pasta.
- Arquivos binários (imagens, fontes) ficam disponíveis para o preview mas não são abertos no editor de texto.
