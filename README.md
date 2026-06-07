# Manual de Física

Livro aberto em [Quarto](https://quarto.org), segundo título da série *Manuais de
Ciências*. Cobre a física do básico ao avançado, em 15 volumes.

**📖 Leia online:** https://vitormattosdev.github.io/manual-fisica/

## Setup em uma máquina nova

Duas ferramentas precisam estar instaladas **localmente** (o conteúdo vem do Git,
mas as ferramentas não):

1. **Quarto** (obrigatório) — <https://quarto.org/docs/get-started/>.
2. **TeX**, só para gerar o **PDF**: `quarto install tinytex`.

Confira a instalação:

```bash
quarto --version
```

## Rodar o site (sem PDF, sem TeX)

```bash
quarto preview
```

Abre o site local com hot-reload. Gera **só HTML**, então não precisa de TeX —
ideal para escrever e revisar capítulos no dia a dia.

## Gerar tudo (site + PDF)

```bash
quarto render
```

Sai em `_book/`. O PDF exige TeX (passo 2 acima). Se você não tem TeX e quer
evitar o erro, comente o bloco `pdf:` em `_quarto.yml`.

## Publicação (GitHub Pages)

O deploy é **automático**: todo `push` na branch `main` dispara o GitHub Action
em `.github/workflows/publish.yml`, que renderiza (incluindo o PDF, via TinyTeX
na nuvem) e publica na branch `gh-pages`.

Configuração de primeira vez:

1. Troque `SEU-USUARIO` no `_quarto.yml` pelo seu usuário/organização.
2. No primeiro deploy, inicialize a `gh-pages` rodando `quarto publish gh-pages`
   uma vez (isso renderiza o PDF e portanto pede TeX local).
3. No GitHub: **Settings → Pages → Source: Deploy from a branch**, escolha a
   branch **`gh-pages`** com a pasta **`/ (root)`**.

## Estrutura

Veja `CLAUDE.md` (como o projeto funciona), `PLANO.md` (guia de estilo) e
`ROADMAP.md` (o plano completo, capítulo a capítulo).

## (Opcional) Diagramas TikZ no HTML

Diagramas físicos em TikZ renderizam no PDF nativamente. Para que apareçam também
no site, instale a extensão:

```bash
quarto add data-intuitive/quarto-tikz
```
