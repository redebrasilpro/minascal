# Memória do projeto — Minascal

Arquivo de contexto para retomar o trabalho rapidamente. Resume decisões, estado atual e próximos passos.

_Última atualização: 2026-05-30_

---

## Resumo em uma linha
Redesign do site da Minascal (cal hidratada, Santa Cruz/RJ) com posicionamento ESG real (economia circular: resíduo industrial → cal hidratada). Site estático no GitHub Pages.

## Links essenciais
- **Repo:** https://github.com/redebrasilpro/minascal (conta GitHub: `redebrasilpro`)
- **Site ao vivo:** https://redebrasilpro.github.io/minascal/
- **Site antigo (fonte do conteúdo):** minascal.com.br
- **Pasta local:** `/Users/waldemaravila/projetos/minascal`

---

## Decisões travadas (NÃO reverter sem perguntar)
1. **Localização = Rio de Janeiro** (Santa Cruz). O briefing dizia "Minas Gerais", mas o dado real é RJ. Nome "Minascal" é só herança/origem.
2. **Produtos = somente cal hidratada** (3 tipos reais: CH-III construção, pintura, CH-I industrial). NÃO incluir cal virgem nem calcário como produto.
3. **Números = placeholders plausíveis** marcados "a confirmar", compatíveis com o porte (28 anos, mesma planta). Placeholders atuais: 120 mil t resíduos/ano, 80+ empregos, 500+ pessoas impactadas.
4. **Frase-guia:** "Transformar resíduo em recurso." (recomendada e em uso).
5. **Tom:** ESG real, sem greenwashing. Formal mas acessível.

## Dados reais confirmados
- Fundada em 1998 por **Tião Ávila** — 28 anos de operação
- Norma **NBR 7175/2003 (ABNT)**
- Endereço: Av. João XXIII s/n, Distrito Industrial de Santa Cruz — Rio de Janeiro — CEP 23.570-000
- E-mail: vendas@minascal.com.br · Tel/WhatsApp: (21) 2418-1088
- Processo: blendagem de resíduos industriais + cal virgem + aditivos → cal hidratada
- Parcerias sociais: **Instituto Casa do Pai**, **Cooperativa Recicla Mais**; contrata egresso de Comunidade Terapêutica

---

## Estado atual (o que está pronto)
- ✅ **Fase 1** — estrutura (5 páginas) + copy ESG (em `conteudo-fase1.md`)
- ✅ **Fase 2** — template HTML/CSS/JS completo, responsivo, publicado no GitHub Pages
- ✅ Documentação: `README.md`, `PROJETO.md`
- ✅ GitHub Pages ativo (branch `main`, root)

## Arquitetura (5 páginas)
`index.html` (Home) · `esg.html` (central E/S/G) · `sobre.html` · `produtos.html` · `contato.html`
- CSS compartilhado: `css/style.css` (paleta em `:root`)
- JS: `js/main.js` (menu mobile, contadores, reveal, formulário sem backend)

---

## Pendências (o que falta — depende do cliente)
1. **Números reais** para substituir os placeholders "a confirmar"
2. **Liderança** — nomes, cargos, fotos (em `sobre.html`)
3. **Relatório de Sustentabilidade** — hoje "Em breve" em `esg.html`
4. **Fotos reais** da operação (hoje usa Unsplash via URL no `style`/`<img>`)
5. **Domínio próprio** — apontar `minascal.com.br` para o Pages quando oficializar

---

## Notas técnicas / ambiente
- **Git identity:** o repo não tem user.name/email configurado. Commits feitos com flags inline:
  `git -c user.name="Waldemar Avila" -c user.email="waldemar@minascal.com.br" commit ...`
- **gh CLI:** instalado em `~/.local/bin/gh` (não está no PATH). Autenticado como `redebrasilpro` (escopo repo). Credential helper configurado → `git push` funciona sem novo login.
- **Push pode exigir** `dangerouslyDisableSandbox` (rede bloqueada no sandbox padrão).
- **GitHub Pages** ativado via API: `gh api -X POST repos/redebrasilpro/minascal/pages -f "source[branch]=main" -f "source[path]=/"`
- **Servidor local:** `python3 -m http.server` (config em `.claude/launch.json`, porta 8732 — mas `.claude/` é gitignored).
- `.gitignore` ignora `.claude/`, `.DS_Store`, `node_modules/`.

## Histórico de commits
- `8a98045` Fase 1 (copy)
- `791773f` Fase 2 (template)
- `8e9620e` PROJETO.md
