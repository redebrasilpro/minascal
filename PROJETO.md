# Projeto Minascal — Site institucional ESG

Documentação geral do projeto de reestruturação e redesign do site da **Minascal**.

---

## 1. Visão geral

Reposicionamento do site da Minascal (fabricante de cal hidratada, Santa Cruz/RJ) com uma narrativa **ESG sólida e crível**, sem greenwashing. O diferencial real da empresa — produzir cal hidratada a partir do **reaproveitamento de resíduos industriais** (economia circular) desde 1998 — é o centro da comunicação.

- **Frase-guia da marca:** *"Transformar resíduo em recurso."*
- **Repositório:** https://github.com/redebrasilpro/minascal
- **Site (preview):** https://redebrasilpro.github.io/minascal/
- **Site atual (referência):** minascal.com.br
- **Natureza:** preview em GitHub Pages, tratado com qualidade de produção.

---

## 2. Fases do projeto

| Fase | Escopo | Status |
|---|---|---|
| **Fase 1** | Reestruturação da arquitetura de informação (5 páginas) + reescrita de toda a copy com pegada ESG | ✅ Concluída |
| **Fase 2** | Template/visual: HTML, CSS, JS, responsividade, paleta, tipografia | ✅ Concluída |
| **Fase 3** | Preenchimento de dados reais + fotos da operação + relatório + domínio próprio | ⏳ Pendente do cliente |

---

## 3. Stack técnica

- **HTML5 + CSS3 + JavaScript vanilla** — sem build, sem backend, sem frameworks
- CSS com variáveis em `:root` (paleta ESG facilmente ajustável)
- Responsivo, **mobile-first**
- Google Fonts: **Fraunces** (títulos) + **Inter** (corpo)
- Imagens: Unsplash (substituir por fotos reais da operação)
- Hospedagem: **GitHub Pages** (`.nojekyll` para servir sem Jekyll)

---

## 4. Estrutura de arquivos

```
minascal/
├── index.html          # Home — hero, pilares ESG, números, destaques, CTA
├── esg.html            # Compromisso ESG (página central: E / S / G + relatório)
├── sobre.html          # História, missão, visão, valores, localização, liderança
├── produtos.html       # Cal hidratada CH-III, pintura, CH-I + selo NBR
├── contato.html        # Formulário (sem backend), dados de contato e mapa
├── css/
│   └── style.css       # Estilos compartilhados por todas as páginas
├── js/
│   └── main.js         # Menu mobile, contadores animados, reveal, formulário
├── assets/
│   ├── images/         # (para fotos reais futuras)
│   └── icons/          # (para ícones adicionais)
├── README.md           # Guia rápido do repositório
├── PROJETO.md          # Este documento
├── conteudo-fase1.md   # Copy aprovada na Fase 1
├── .nojekyll           # GitHub Pages sem processamento Jekyll
└── .gitignore
```

---

## 5. Mapa do site

Navegação global em todas as páginas: **Home · Sobre · ESG · Produtos · Contato** + botão "Fale conosco".

- **Home (`index.html`)** — hero de posicionamento, resumo institucional, 3 pilares ESG, números de impacto (animados), destaques de sustentabilidade, CTA para ESG.
- **ESG (`esg.html`)** — manifesto + seções Ambiental (E), Social (S) e Governança (G) com badges, indicadores e listas; bloco de Relatório de Sustentabilidade ("Em breve").
- **Sobre (`sobre.html`)** — história desde 1998, Missão/Visão, Valores, localização (Santa Cruz/RJ), liderança (placeholder).
- **Produtos (`produtos.html`)** — 3 linhas de cal hidratada (CH-III, pintura, CH-I), diferenciais e selo NBR 7175/2003.
- **Contato (`contato.html`)** — dados reais, formulário sem backend, mapa do Google embutido.

---

## 6. Identidade visual

### Paleta (variáveis CSS em `css/style.css`)
| Variável | Hex | Uso |
|---|---|---|
| `--verde-principal` | `#2D6A4F` | Verde floresta — ambiental |
| `--verde-claro` | `#52B788` | Botões, destaques |
| `--terra` | `#8B5E3C` | Terra/cal — identidade mineral |
| `--bege` | `#F4F1EC` | Fundo quente |
| `--cinza-escuro` | `#1C1C1C` | Textos principais |
| `--dourado-suave` | `#C9A84C` | Acento — selos, destaques |

### Tipografia
- Títulos: **Fraunces** (serifada, sofisticada)
- Corpo: **Inter** (leitura limpa), base 16px, linha 1.6

### Interações (JS)
- Menu hambúrguer no mobile
- Contadores numéricos animados (ao entrar na viewport)
- Reveal suave de elementos no scroll (respeita `prefers-reduced-motion`)
- Formulário de contato com feedback (demonstração, sem envio real)

---

## 7. Dados reais utilizados

- **Fundação:** 1998, por Tião Ávila — 28 anos de operação
- **Norma:** NBR 7175/2003 (ABNT)
- **Endereço:** Av. João XXIII s/n, Distrito Industrial de Santa Cruz — Rio de Janeiro — CEP 23.570-000
- **E-mail:** vendas@minascal.com.br
- **Telefone/WhatsApp:** (21) 2418-1088
- **Produtos:** Cal Hidratada CH-III (construção), para Pintura e CH-I (industrial)
- **Parcerias sociais:** Instituto Casa do Pai, Cooperativa Recicla Mais
- **Processo:** blendagem de resíduos industriais + cal virgem + aditivos → cal hidratada

---

## 8. Pendências (marcadas "a confirmar" no site)

1. **Números de impacto** — toneladas de resíduos reaproveitadas/ano, empregos gerados, pessoas impactadas (hoje placeholders: 120 mil t, 80+ empregos, 500+ pessoas).
2. **Liderança** — nomes, cargos e fotos (`sobre.html`).
3. **Relatório de Sustentabilidade** — link/PDF (hoje "Em breve" em `esg.html`).
4. **Fotos reais** da operação (substituir imagens Unsplash).
5. **Domínio próprio** — apontar `minascal.com.br` para o GitHub Pages, quando tornar oficial.

---

## 9. Como rodar e publicar

### Localmente
```bash
python3 -m http.server 8000
# acesse http://localhost:8000
```

### GitHub Pages
Já ativo. Configuração: **Settings → Pages → branch `main` / root**.
URL: https://redebrasilpro.github.io/minascal/

---

## 10. Histórico de commits

- `8a98045` — Fase 1: estrutura e copy ESG
- `791773f` — Fase 2: template do site (HTML/CSS/JS)
