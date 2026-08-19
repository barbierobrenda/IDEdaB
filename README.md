# Brenda IDE

IDE web estática para editar arquivos HTML e visualizar o resultado em tempo real.

## Recursos
- Editor HTML
- Preview em tempo real
- Autosave no navegador
- Abrir arquivo `.html`
- Baixar o HTML editado
- Layout dividido em desktop/iPad horizontal
- Abas Código/Preview em telas menores
- PWA instalável na Tela de Início
- Funciona hospedada no GitHub Pages

## Publicar no GitHub Pages
1. Crie um repositório, por exemplo `brenda-ide`.
2. Envie `index.html`, `manifest.json` e `sw.js`.
3. No GitHub, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha `main` e `/ (root)`.
6. Salve.
7. Abra a URL do GitHub Pages no iPad.
8. No Safari, use **Compartilhar → Adicionar à Tela de Início**.

## Importante
O autosave usa o armazenamento local do navegador. Cada dispositivo mantém sua própria cópia.
Para versionar alterações no GitHub, baixe o `.html` e faça o commit pelo GitHub ou por um editor conectado ao repositório.
