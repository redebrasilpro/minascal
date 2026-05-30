# CLAUDE.md

Orientações para o Claude Code ao trabalhar neste repositório.

## O que é
Site institucional estático da **Minascal** (fabricante de cal hidratada, Santa Cruz/RJ) com posicionamento **ESG real** — economia circular: resíduo industrial → cal hidratada, desde 1998. Hospedado em GitHub Pages.

- Repo: `redebrasilpro/minascal` · Site: https://redebrasilpro.github.io/minascal/
- Para contexto completo e estado do projeto, leia **`memoria.md`** primeiro. Visão geral em `PROJETO.md`; copy aprovada em `conteudo-fase1.md`.

## Stack e arquitetura
- **HTML5 + CSS3 + JavaScript vanilla.** Sem build, sem backend, sem frameworks, sem dependências npm. Deve rodar abrindo o HTML direto / no GitHub Pages.
- 5 páginas na raiz: `index.html`, `esg.html`, `sobre.html`, `produtos.html`, `contato.html`.
- CSS único compartilhado: `css/style.css` (paleta em `:root`). JS único: `js/main.js`.
- Header e footer são **repetidos em cada HTML** (não há templating). Ao alterar nav/footer, replicar em **todas as 5 páginas** e manter a classe `active` correta no link da página atual.

## Comandos
```bash
# Servir localmente
python3 -m http.server 8000      # http://localhost:8000

# Git: o repo NÃO tem user configurado — use identidade inline
git -c user.name="Waldemar Avila" -c user.email="waldemar@minascal.com.br" commit -m "..."

# gh CLI fica em ~/.local/bin (fora do PATH); autenticado como redebrasilpro
~/.local/bin/gh ...
```
- `git push` e chamadas de rede podem exigir `dangerouslyDisableSandbox: true` (sandbox bloqueia rede).
- Não há testes nem linters configurados.

## Convenções
- **Idioma:** todo o conteúdo em **PT-BR**.
- **Estilo:** usar variáveis CSS de `:root`; mobile-first; classes utilitárias já existentes (`.section`, `.container`, `.grid--3`, `.card`, `.btn`, `.reveal`, etc.). Evitar CSS inline novo quando já houver utilitário.
- **Acessibilidade:** manter `alt` em imagens, `aria-*` na nav e respeitar `prefers-reduced-motion`.
- Imagens hoje vêm do Unsplash via URL; ao receber fotos reais, colocar em `assets/images/`.

## Restrições / decisões travadas (NÃO reverter sem perguntar)
1. **Localização = Rio de Janeiro** (Santa Cruz). Nunca "Minas Gerais" — o nome é só herança.
2. **Produtos = somente cal hidratada** (CH-III, pintura, CH-I). Não inventar cal virgem/calcário como produto.
3. **Números são placeholders** marcados "a confirmar" — manter o marcador até o cliente validar.
4. **Frase-guia:** "Transformar resíduo em recurso."
5. **Tom ESG real, sem greenwashing.** Sempre ligar produto → benefício ambiental/social concreto.

## Ao concluir mudanças
- Verificar consistência entre as 5 páginas (nav, footer, CSS/JS referenciados).
- Conferir que links internos apontam para arquivos existentes.
- Commitar e dar push (o cliente prefere tudo versionado no GitHub).
- Se mudar decisões/estado relevante, atualizar `memoria.md`.
