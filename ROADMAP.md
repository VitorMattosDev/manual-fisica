# ROADMAP — Manual de Física

Plano completo da obra, capítulo a capítulo, em ordem de execução. Este arquivo é
a **fila de trabalho**: define exatamente o que criar, em que volume, com que nome
de arquivo e em que ordem, do começo ao fim.

- **ROADMAP.md** (este arquivo) = *o quê / em que ordem*
- **PLANO.md** = *como escrever* (estilo, ambientes, convenções)
- **CLAUDE.md** = as regras que amarram os dois

## Protocolo de execução (para o agente)

A próxima tarefa é **sempre o primeiro item `[ ]` não marcado**, na ordem abaixo.
Para executá-la:

1. Use exatamente o **caminho de arquivo** indicado no item.
2. Mostre primeiro um **esboço da estrutura** (seções, definições, leis, exemplos)
   e espere aprovação antes de escrever o capítulo completo.
3. Escreva seguindo o `PLANO.md` e espelhando o gabarito
   `volumes/v2-mecanica1/06-conservacao-energia.qmd`.
4. Registre o `.qmd` em `chapters:` do `_quarto.yml` (descomentando/criando o
   bloco `part:` do volume, se necessário).
5. Atualize `constantes.qmd` se introduzir constantes ou fórmulas novas.
6. Rode `quarto render` (ou `quarto preview` se não houver TeX) para confirmar
   que compila.
7. Marque o item como `[x]` aqui e faça um **commit** pequeno e descritivo.

**Estratégia da fatia vertical:** feche um volume inteiro antes de abrir o
próximo. E **conclua toda a Fase 1 antes de iniciar a Fase 2.**

Estado atual: **1** pronto (gabarito), **92** pendentes.

---

# FASE 1 — Física Clássica

## Volume I — Fundamentos da Física
*Objetivo: a linguagem da física. Pré-requisitos: nenhum.*

- [x] `volumes/v1-fundamentos/01-grandezas-unidades.qmd` — Grandezas, SI e conversões
- [x] `volumes/v1-fundamentos/02-analise-dimensional.qmd` — Análise dimensional
- [x] `volumes/v1-fundamentos/03-medicao-erros.qmd` — Medição, algarismos significativos, teoria de erros
- [x] `volumes/v1-fundamentos/04-vetores.qmd` — Vetores e álgebra vetorial
- [x] `volumes/v1-fundamentos/05-ferramentas-calculo.qmd` — Derivadas e integrais na física
- [x] `volumes/v1-fundamentos/06-modelagem.qmd` — Modelagem e método científico

## Volume II — Mecânica Clássica I (Cinemática e Dinâmica)
*Objetivo: descrever e prever o movimento. Pré-requisitos: I.*

- [x] `volumes/v2-mecanica1/01-cinematica-1d.qmd` — Cinemática unidimensional
- [x] `volumes/v2-mecanica1/02-cinematica-vetorial.qmd` — Vetorial, projéteis, circular
- [x] `volumes/v2-mecanica1/03-leis-newton.qmd` — Leis de Newton
- [x] `volumes/v2-mecanica1/04-aplicacoes-newton.qmd` — Atrito e aplicações
- [x] `volumes/v2-mecanica1/05-trabalho-energia.qmd` — Trabalho e energia
- [x] `volumes/v2-mecanica1/06-conservacao-energia.qmd` — Conservação de energia (GABARITO)
- [x] `volumes/v2-mecanica1/07-momento-linear.qmd` — Momento linear e colisões
- [x] `volumes/v2-mecanica1/08-centro-massa.qmd` — Centro de massa e sistemas de partículas

## Volume III — Mecânica Clássica II (Rotação, Gravitação, Oscilações)
*Objetivo: corpos extensos, órbitas e vibrações. Pré-requisitos: II.*

- [x] `volumes/v3-mecanica2/01-cinematica-rotacional.qmd` — Cinemática rotacional
- [x] `volumes/v3-mecanica2/02-dinamica-rotacional.qmd` — Torque e dinâmica rotacional
- [x] `volumes/v3-mecanica2/03-momento-angular.qmd` — Momento angular
- [x] `volumes/v3-mecanica2/04-estatica-corpos-rigidos.qmd` — Estática e corpos rígidos
- [x] `volumes/v3-mecanica2/05-gravitacao.qmd` — Gravitação universal (Newton, Kepler)
- [x] `volumes/v3-mecanica2/06-mhs.qmd` — Movimento harmônico simples
- [x] `volumes/v3-mecanica2/07-oscilacoes-amortecidas.qmd` — Amortecidas, forçadas, ressonância

## Volume IV — Fluidos e Meios Contínuos
*Objetivo: matéria que flui e deforma. Pré-requisitos: II.*

- [x] `volumes/v4-fluidos/01-estatica-fluidos.qmd` — Estática (pressão, empuxo)
- [x] `volumes/v4-fluidos/02-dinamica-fluidos.qmd` — Continuidade e Bernoulli
- [x] `volumes/v4-fluidos/03-viscosidade.qmd` — Viscosidade e fluidos reais
- [x] `volumes/v4-fluidos/04-elasticidade.qmd` — Elasticidade e deformação dos sólidos

## Volume V — Ondas e Acústica
*Objetivo: perturbações que se propagam. Pré-requisitos: III (MHS).*

- [x] `volumes/v5-ondas/01-movimento-ondulatorio.qmd` — Movimento ondulatório
- [x] `volumes/v5-ondas/02-ondas-meios.qmd` — Ondas em cordas e meios
- [x] `volumes/v5-ondas/03-superposicao-interferencia.qmd` — Superposição e interferência
- [x] `volumes/v5-ondas/04-ondas-estacionarias.qmd` — Ondas estacionárias e ressonância
- [x] `volumes/v5-ondas/05-som-acustica.qmd` — Som e acústica
- [x] `volumes/v5-ondas/06-efeito-doppler.qmd` — Efeito Doppler

## Volume VI — Termodinâmica e Física Estatística
*Objetivo: calor, entropia e o mundo dos muitos corpos. Pré-requisitos: II.*

- [x] `volumes/v6-termodinamica/01-temperatura-dilatacao.qmd` — Temperatura e dilatação
- [x] `volumes/v6-termodinamica/02-calor-primeira-lei.qmd` — Calor e primeira lei
- [x] `volumes/v6-termodinamica/03-teoria-cinetica.qmd` — Teoria cinética dos gases
- [x] `volumes/v6-termodinamica/04-segunda-lei-entropia.qmd` — Segunda lei e entropia
- [x] `volumes/v6-termodinamica/05-ciclos-maquinas.qmd` — Ciclos e máquinas térmicas
- [x] `volumes/v6-termodinamica/06-transicoes-fase.qmd` — Transições de fase
- [x] `volumes/v6-termodinamica/07-fisica-estatistica.qmd` — Introdução à física estatística

## Volume VII — Eletromagnetismo I (Eletrostática e Corrente)
*Objetivo: cargas, campos e circuitos DC. Pré-requisitos: I (vetores, cálculo).*

- [x] `volumes/v7-eletromagnetismo1/01-carga-coulomb.qmd` — Carga e lei de Coulomb
- [x] `volumes/v7-eletromagnetismo1/02-campo-eletrico.qmd` — Campo elétrico
- [x] `volumes/v7-eletromagnetismo1/03-lei-gauss.qmd` — Lei de Gauss
- [x] `volumes/v7-eletromagnetismo1/04-potencial-eletrico.qmd` — Potencial elétrico
- [x] `volumes/v7-eletromagnetismo1/05-capacitancia.qmd` — Capacitância e dielétricos
- [x] `volumes/v7-eletromagnetismo1/06-corrente-resistencia.qmd` — Corrente, resistência, Ohm
- [x] `volumes/v7-eletromagnetismo1/07-circuitos-dc.qmd` — Circuitos DC (Kirchhoff, RC)

## Volume VIII — Eletromagnetismo II (Magnetismo e Maxwell)
*Objetivo: do magnetismo às ondas EM. Pré-requisitos: VII.*

- [x] `volumes/v8-eletromagnetismo2/01-campo-magnetico.qmd` — Campo magnético e força de Lorentz
- [x] `volumes/v8-eletromagnetismo2/02-fontes-campo-magnetico.qmd` — Biot-Savart e Ampère
- [x] `volumes/v8-eletromagnetismo2/03-inducao-eletromagnetica.qmd` — Faraday e Lenz
- [x] `volumes/v8-eletromagnetismo2/04-indutancia.qmd` — Indutância
- [x] `volumes/v8-eletromagnetismo2/05-circuitos-ac.qmd` — Circuitos AC e RLC
- [x] `volumes/v8-eletromagnetismo2/06-equacoes-maxwell.qmd` — Equações de Maxwell
- [x] `volumes/v8-eletromagnetismo2/07-ondas-eletromagneticas.qmd` — Ondas eletromagnéticas

## Volume IX — Óptica
*Objetivo: comportamento da luz. Pré-requisitos: V (ondas), VIII (ondas EM).*

- [x] `volumes/v9-optica/01-natureza-luz.qmd` — Natureza e propagação da luz
- [x] `volumes/v9-optica/02-optica-geometrica.qmd` — Reflexão e refração
- [x] `volumes/v9-optica/03-espelhos-lentes.qmd` — Espelhos, lentes, instrumentos
- [ ] `volumes/v9-optica/04-interferencia.qmd` — Interferência (Young, filmes finos)
- [ ] `volumes/v9-optica/05-difracao.qmd` — Difração
- [ ] `volumes/v9-optica/06-polarizacao.qmd` — Polarização

## Volume X — Relatividade Especial
*Objetivo: espaço-tempo. Pré-requisitos: III, VIII. (Matemática: ver nota.)*

- [ ] `volumes/v10-relatividade/01-postulados-cinematica.qmd` — Postulados e cinemática relativística
- [ ] `volumes/v10-relatividade/02-dilatacao-contracao.qmd` — Dilatação do tempo e contração
- [ ] `volumes/v10-relatividade/03-dinamica-relativistica.qmd` — Energia-momento
- [ ] `volumes/v10-relatividade/04-quadrivetores-minkowski.qmd` — Quadrivetores e Minkowski
- [ ] `volumes/v10-relatividade/05-ponte-relatividade-geral.qmd` — Princípio da equivalência (ponte p/ RG)

---

# FASE 2 — Física Moderna e Avançada

> **Só iniciar após toda a Fase 1 estar marcada `[x]` e o projeto compilar.**

## Volume XI — Mecânica Analítica
*Objetivo: reformular a mecânica. Pré-requisitos: III. (Matemática: cálculo variacional.)*

- [ ] `volumes/v11-mecanica-analitica/01-calculo-variacional.qmd` — Cálculo variacional e princípio de Hamilton
- [ ] `volumes/v11-mecanica-analitica/02-lagrangiana.qmd` — Formulação lagrangiana e vínculos
- [ ] `volumes/v11-mecanica-analitica/03-aplicacoes-lagrangiana.qmd` — Aplicações lagrangianas
- [ ] `volumes/v11-mecanica-analitica/04-hamiltoniana.qmd` — Formulação hamiltoniana
- [ ] `volumes/v11-mecanica-analitica/05-transformacoes-canonicas.qmd` — Transformações canônicas e Poisson
- [ ] `volumes/v11-mecanica-analitica/06-hamilton-jacobi.qmd` — Hamilton-Jacobi e ação-ângulo

## Volume XII — Mecânica Quântica
*Objetivo: o mundo quântico. Pré-requisitos: XI, VIII.*

- [ ] `volumes/v12-quantica/01-origens-quantica.qmd` — Origens (corpo negro, fotoelétrico, Bohr)
- [ ] `volumes/v12-quantica/02-dualidade.qmd` — Dualidade onda-partícula (de Broglie)
- [ ] `volumes/v12-quantica/03-equacao-schrodinger.qmd` — Equação de Schrödinger
- [ ] `volumes/v12-quantica/04-pocos-barreiras.qmd` — Poços, barreiras, tunelamento
- [ ] `volumes/v12-quantica/05-formalismo.qmd` — Formalismo (Hilbert, operadores)
- [ ] `volumes/v12-quantica/06-oscilador-harmonico.qmd` — Oscilador harmônico quântico
- [ ] `volumes/v12-quantica/07-momento-angular-spin.qmd` — Momento angular e spin
- [ ] `volumes/v12-quantica/08-atomo-hidrogenio.qmd` — Átomo de hidrogênio
- [ ] `volumes/v12-quantica/09-metodos-aproximados.qmd` — Teoria de perturbação

## Volume XIII — Física Atômica, Molecular e da Matéria Condensada
*Objetivo: da estrutura atômica aos sólidos. Pré-requisitos: XII.*

- [ ] `volumes/v13-materia/01-estrutura-atomica.qmd` — Estrutura atômica e tabela periódica
- [ ] `volumes/v13-materia/02-espectros.qmd` — Espectros atômicos
- [ ] `volumes/v13-materia/03-moleculas-ligacoes.qmd` — Moléculas e ligações
- [ ] `volumes/v13-materia/04-estatistica-quantica.qmd` — Fermi-Dirac e Bose-Einstein
- [ ] `volumes/v13-materia/05-estado-solido.qmd` — Bandas e semicondutores
- [ ] `volumes/v13-materia/06-supercondutividade.qmd` — Supercondutividade

## Volume XIV — Física Nuclear e de Partículas
*Objetivo: o núcleo e o que é fundamental. Pré-requisitos: XII.*

- [ ] `volumes/v14-nuclear-particulas/01-estrutura-nuclear.qmd` — Estrutura nuclear
- [ ] `volumes/v14-nuclear-particulas/02-radioatividade.qmd` — Radioatividade e decaimento
- [ ] `volumes/v14-nuclear-particulas/03-reacoes-nucleares.qmd` — Reações, fissão e fusão
- [ ] `volumes/v14-nuclear-particulas/04-particulas-elementares.qmd` — Partículas e Modelo Padrão
- [ ] `volumes/v14-nuclear-particulas/05-interacoes-fundamentais.qmd` — Interações fundamentais

## Volume XV — Tópicos Avançados
*Objetivo: as fronteiras. Pré-requisitos: X, XII. (Matemática: geometria riemanniana p/ RG.)*

- [ ] `volumes/v15-avancados/01-relatividade-geral.qmd` — Relatividade geral (métrica, geodésicas, Einstein)
- [ ] `volumes/v15-avancados/02-teoria-quantica-campos.qmd` — Introdução à teoria quântica de campos
- [ ] `volumes/v15-avancados/03-cosmologia.qmd` — Cosmologia
- [ ] `volumes/v15-avancados/04-astrofisica.qmd` — Astrofísica
