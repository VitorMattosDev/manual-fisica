# CLAUDE.md — Manual de Física

Livro aberto em **Quarto**, segundo título da série *Manuais de Ciências*. Vai dos
fundamentos (unidades, vetores) à física avançada (relatividade geral, TQC,
cosmologia). Publicado no GitHub Pages.

## Comandos

```bash
quarto preview     # site local com hot-reload (só HTML) — uso diário
quarto render      # gera site + PDF em _book/ (PDF exige TeX)
quarto publish gh-pages   # render + deploy manual (raramente necessário)
```

- O deploy normal é **automático**: todo `push` na `main` dispara o GitHub Action
  (`.github/workflows/publish.yml`), que renderiza e publica (com PDF, via
  TinyTeX na nuvem).
- **PDF exige TeX local** (`quarto install tinytex`). Sem TeX, o render do formato
  PDF falha. Para trabalhar só no site numa máquina sem TeX, use `quarto preview`
  (que só gera HTML) ou comente o bloco `pdf:` em `_quarto.yml`.

## Estrutura

```
_quarto.yml    configuração do livro (lang: pt no NÍVEL RAIZ, nunca em book:)
index.qmd      apresentação + grafo de pré-requisitos (mermaid)
constantes.qmd apêndice de constantes físicas e formulário
PLANO.md       guia de estilo — COMO escrever (FONTE DA VERDADE do estilo)
ROADMAP.md     fila executável capítulo a capítulo — O QUÊ / em que ordem
volumes/       capítulos, em volumes/vN-tema/NN-nome.qmd
```

## O que construir (roadmap)

Ao receber "escreva o próximo capítulo": abra o `ROADMAP.md`, pegue o **primeiro
item `[ ]` não marcado**, siga o **protocolo de execução** que está no topo dele
(mostrar esboço → aprovar → escrever → registrar no `_quarto.yml` → render →
marcar `[x]` → commit). Feche um volume antes de abrir o próximo; conclua a Fase 1
inteira antes da Fase 2.

## Convenções de escrita (sempre seguir — detalhe em PLANO.md)

- Gabarito de estilo: `volumes/v2-mecanica1/06-conservacao-energia.qmd`. Espelhe-o.
- Estrutura do capítulo: Motivação → Definições → Leis/Equações → Dedução →
  Exemplos resolvidos → Exercícios → Soluções.
- Idioma **português**; **decimal com vírgula** (`$9{,}8$`).
- Ambientes: `def-` definição · `exm-` exemplo · `exr-` exercício · `.proof` dedução.
  Leis/Princípios em `::: {.callout-important}` com a equação numerada dentro.
  Solução de exercício em `::: {.callout-note collapse="true"}`.
- Equações importantes sempre numeradas (`$$...$$ {#eq-nome}`) e referenciadas com
  `@eq-nome`. **Nunca** escreva o número na mão.
- **Unidades com `\mathrm{}` + `\,`** (ex.: `$9{,}8\ \mathrm{m/s^2}$`). **Proibido**
  `siunitx` e macros do pacote `physics` — quebram o HTML.

## Regras do projeto

- Ao adicionar capítulo: criar o `.qmd` E registrá-lo em `chapters:` do
  `_quarto.yml`. Para abrir um volume novo, descomentar/criar o bloco `part:`
  (há um template comentado no fim do `_quarto.yml`).
- Mantenha `constantes.qmd` e o `ROADMAP.md` atualizados ao introduzir constantes,
  fórmulas ou concluir capítulos.
- Antes de propor reestruturação grande, consulte `ROADMAP.md` e `PLANO.md`.
- Commits pequenos e descritivos, um por capítulo concluído.
- **Cuidado redobrado na revisão** (sobretudo Fase 2): confira convenções de
  sinal, unidades e hipóteses físicas. Revise o `diff` antes de cada commit.

## Estado atual

- **Obra completa.** Todos os 93 capítulos (Volumes I a XV, Fases 1 e 2) escritos,
  registrados no `_quarto.yml` e marcados `[x]` no `ROADMAP.md`. O projeto compila
  em HTML e em PDF (render completo validado). `constantes.qmd` consolida o
  formulário de toda a obra.
- Manutenção daqui em diante: revisões, correções e eventuais novos apêndices.
  Ao editar matemática inline, lembre-se de **não deixar espaço antes do `$` de
  fechamento** (o Pandoc não reconhece como matemática e quebra o PDF).
