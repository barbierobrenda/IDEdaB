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

## v3.4 Purple Minimal
- Identidade roxa, com tema claro e escuro (botão 🌙/☀ no cabeçalho, lembrado entre sessões).
- Editor com realce de sintaxe colorido (CodeMirror), tema Dracula no modo escuro e Eclipse no modo claro.
- Suporte a muito mais tipos de arquivo além de HTML: CSS, JS/JSX/TS/TSX, JSON, Markdown, XML/SVG, Python, PHP, SQL, YAML, Shell, C/C++, Java, Ruby, Go e Rust — tanto ao abrir do dispositivo quanto do GitHub.
- A linguagem detectada aparece como uma etiqueta ao lado do título do editor.
- Preview em tempo real continua específico para HTML/PHP; outros tipos aparecem formatados como texto no painel de preview.
