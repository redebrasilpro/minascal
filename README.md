# Minascal — Site institucional ESG

Site estático da **Minascal**, fabricante de cal hidratada (Santa Cruz, Rio de Janeiro) com posicionamento ESG real: produção a partir do **reaproveitamento de resíduos industriais** desde 1998.

> Frase-guia da marca: **"Transformar resíduo em recurso."**

## Stack
- HTML5 + CSS3 + JavaScript vanilla (sem build, sem backend)
- CSS com variáveis em `:root` (paleta ESG facilmente ajustável)
- Responsivo, mobile-first
- Google Fonts: **Fraunces** (títulos) + **Inter** (corpo)
- Imagens via Unsplash (substituir por fotos reais da operação na produção)

## Estrutura
```
.
├── index.html        # Home — hero, pilares ESG, números, destaques
├── esg.html          # Compromisso ESG (página central: E / S / G)
├── sobre.html        # História, missão, visão, valores, liderança
├── produtos.html     # Cal hidratada CH-III, pintura e CH-I
├── contato.html      # Formulário (sem backend), dados e mapa
├── css/style.css     # Estilos compartilhados
├── js/main.js        # Menu mobile, contadores, reveal, formulário
├── assets/           # images/ e icons/ (para fotos reais futuras)
├── .nojekyll         # Serve arquivos no GitHub Pages sem Jekyll
└── conteudo-fase1.md # Copy aprovada (Fase 1)
```

## Rodar localmente
Por ser 100% estático, basta abrir `index.html` no navegador. Para testar com servidor local:
```bash
python3 -m http.server 8000
# acesse http://localhost:8000
```

## Publicar no GitHub Pages
1. Repositório → **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main` / `/ (root)` → Save
4. URL: `https://redebrasilpro.github.io/minascal/`

## Pendências de conteúdo (`[a confirmar]`)
Estes itens usam **placeholders plausíveis** e precisam de validação antes da publicação oficial:
- Números de impacto: toneladas de resíduos reaproveitadas/ano, empregos gerados, pessoas impactadas (marcados como *"a confirmar"* no site)
- Liderança: nomes, cargos e fotos (`sobre.html`)
- Relatório de Sustentabilidade: link/PDF (hoje "Em breve" em `esg.html`)
- Fotos reais da operação (substituir as imagens Unsplash)

## Dados reais utilizados
- Fundação: 1998, por Tião Ávila — 28 anos de operação
- Norma: NBR 7175/2003 (ABNT)
- Endereço: Av. João XXIII s/n, Distrito Industrial de Santa Cruz — Rio de Janeiro — CEP 23.570-000
- E-mail: vendas@minascal.com.br · Tel/WhatsApp: (21) 2418-1088
- Produtos: Cal Hidratada CH-III (construção), para Pintura e CH-I (industrial)
- Parcerias sociais: Instituto Casa do Pai, Cooperativa Recicla Mais
