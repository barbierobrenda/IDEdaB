# Brenda IDE v4 — Multi-arquivo

## Novidades da v4
- **Abas**: abra vários arquivos ao mesmo tempo (HTML, CSS, JS, JSON, Markdown, texto), cada um em sua própria aba, e alterne entre eles sem perder o que estava editando.
- Toque em **+ Aba** (no cabeçalho) ou no **+** no final da barra de abas para criar um arquivo em branco; use **Abrir** para importar vários arquivos do dispositivo de uma vez.
- Cada aba tem uma bolinha colorida por tipo de arquivo e um indicador de alterações não commitadas.
- **GitHub**: cada arquivo aberto do repositório vira sua própria aba, com repositório/branch/caminho independentes — dá para editar e commitar vários arquivos do mesmo repo sem perder o contexto de cada um.
- **Backup** agora baixa todas as abas abertas em um único arquivo `.json`.
- Aparência renovada: tipografia Inter/JetBrains Mono, mais contraste e profundidade no tema escuro, foco visível no teclado e cores por linguagem nas abas.

## Recursos existentes
- Preview em tempo real para celular/tablet/desktop (somente para arquivos HTML).
- Busca, formatação de HTML, copiar código, backup e atualização com backup.
- Integração opcional com GitHub: listar repositórios com permissão de push, navegar em pastas, abrir arquivos e commitar.
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
