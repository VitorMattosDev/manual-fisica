# PLANO — Guia de Estilo do Manual de Física

Este arquivo define **como** escrever cada capítulo. O **que** escrever e em que
ordem está no `ROADMAP.md`. O capítulo-gabarito é
`volumes/v2-mecanica1/06-conservacao-energia.qmd` — ao escrever qualquer capítulo,
espelhe a estrutura, os ambientes e o tom dele.

## Tom e idioma

- Idioma **português**. Tom **didático antes de formal**: sempre motivar
  fisicamente antes de definir; explicar o porquê antes do como.
- **Decimal com vírgula**, em matemática inclusive: escreva `$9{,}8$`, não `$9.8$`.
  Os chaves em `{,}` mantêm o espaçamento correto.

## Estrutura padrão do capítulo

1. **Motivação** — um fenômeno ou problema concreto que o capítulo vai explicar.
2. **Conceitos e definições** — grandezas novas, em ambientes `def-`.
3. **Leis e equações fundamentais** — em caixas `callout-important` tituladas,
   contendo a equação numerada.
4. **Dedução** — em ambiente `.proof` ou seção própria, quando cabível.
5. **Exemplo(s) resolvido(s)** — em `exm-`, sempre com números e unidades.
6. **Exercícios** — em `exr-`, com solução em caixa colapsável logo abaixo.

## Ambientes (numeram e referenciam sozinhos)

- `::: {#def-nome}` definição · `::: {#exm-nome}` exemplo · `::: {#exr-nome}` exercício
- `::: {.proof}` dedução/demonstração (encerre com `$\qquad\blacksquare$`)
- **Leis/Princípios**: NÃO existe ambiente "teorema" idiomático para física aqui.
  Use uma caixa titulada e coloque a equação-chave numerada dentro:
  ```
  ::: {.callout-important}
  ## Segunda Lei de Newton
  $$\vec{F}_\text{res} = m\vec{a}.$$ {#eq-newton2}
  :::
  ```
- **Solução de exercício**: caixa colapsável logo após o `exr-`:
  ```
  ::: {.callout-note collapse="true"}
  ## Solução
  ...
  :::
  ```

## Referências cruzadas (nunca escrever o número na mão)

- `@def-nome` → "Definição 6.1" · `@exm-nome` → "Exemplo 6.1" · `@eq-nome` → "Equação 6.3".
- Numere **toda** equação importante com `$$...$$ {#eq-nome}` para poder referenciá-la.

## Matemática e unidades

- `$...$` em linha, `$$...$$` em destaque.
- **Unidades via `\mathrm{}` e espaço fino `\,`**, p.ex. `$9{,}8\ \mathrm{m/s^2}$`.
  **Não use o pacote `siunitx` nem macros do pacote `physics`** (`\qty`, `\dv`,
  `\pdv`): eles funcionam só no PDF e **quebram o site HTML** (MathJax). Tudo que
  for escrito deve renderizar nos dois formatos.

## Figuras

- Diagramas conceituais/fluxos: **mermaid** (renderiza em HTML e PDF).
- Diagramas físicos (corpo livre, circuitos): **TikZ/CircuiTikZ**. Render em PDF é
  nativo; para o HTML é preciso instalar a extensão `quarto-tikz` (passo opcional,
  documentado no README). Enquanto a extensão não estiver instalada, **descreva** a
  figura em texto e deixe um comentário `<!-- TODO figura -->` no lugar, para não
  quebrar o `quarto preview`.
- Sempre dê legenda e numere: `![Legenda.](caminho){#fig-nome}` e referencie com `@fig-nome`.

## Bibliografia

- Ainda não há `referencias.bib` configurado (para o scaffold compilar sem
  dependências). Quando quiser citações, crie o `.bib`, adicione
  `bibliography: referencias.bib` ao `_quarto.yml` e use `@chave`.
