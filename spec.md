# Especificação Técnica – Página “IA para Desenvolvedores” (G‑Sites)

## 1. Visão Geral

Página HTML simples para ser incorporada em um Google Sites, servindo como hub da disciplina **IA para Desenvolvedores**, com:

- Foco em baixa carga cognitiva e clareza para o aluno.
- Visual inspirado na trilha oficial **IA para DEVs – SCTEC**, apenas como referência de cores/estética.
- Conteúdo estrutural completo apenas para a **Aula 1**; demais aulas, links, materiais e simulados entram como placeholders.

Organizacao de arquivos no repositorio:

- A pagina HTML final fica em `ia-para-desenvolvedores.html`.
- As especificacoes oficiais ficam em `spec.md`.
- Conteudos das aulas apresentadas ficam em `assets/aulas/` (ex.: `assets/aulas/aula1.md`).

---

## 2. Stack e Restrições Técnicas

- HTML5 puro, compatível com incorporação no Google Sites.  
  - Status: `STATUS_REFINADO`
- CSS simples, preferencialmente em `<style>` interno dentro do `<head>` (sem frameworks, sem dependências externas obrigatórias).  
  - Status: `STATUS_REFINADO`
- Nenhum JavaScript obrigatório para funcionamento da página (apenas HTML + CSS).  
  - Status: `STATUS_REFINADO`
- JavaScript opcional apenas para UX em embeds (ex.: botão "Voltar ao início" com `scrollTo` sem alterar URL).  
  - Status: `STATUS_REFINADO`
- Colapsabilidade das seções principais implementada com recursos nativos de HTML (por exemplo, `<details>` e `<summary>`), sem depender de bibliotecas externas.  
  - Status: `STATUS_REFINADO`

---

## 3. Arquitetura de Conteúdo e Componentes

### 3.1. Estrutura Global

- Documento com:
  - `<!DOCTYPE html>`
  - `<html lang="pt-BR">`
  - `<head>` com:
    - `<meta charset="UTF-8">`
    - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
    - `<title>IA para Desenvolvedores – Hub da Disciplina</title>`
    - `<style>…</style>` com todos os estilos.
  - `<body>` contendo todas as seções descritas abaixo, em coluna única centralizada (largura máxima ≈ 800px).
  - Todas as seções principais organizadas em blocos colapsáveis, permitindo que o aluno expanda apenas o que deseja ler em cada momento, reduzindo a carga cognitiva.
- Status: `STATUS_REFINADO`

### 3.2. Header / Hero da Disciplina

- Composição:
  - Título principal (`h1`): “IA para Desenvolvedores”.
  - Subtítulo curto (parágrafo): “Hub da disciplina: aulas, materiais e simulados” (texto pode ser ajustado pelo professor).
  - Opcional: pequena área de tags (chips) com no máximo 2 itens, por exemplo:
    - “Avançado”
    - “Síncrono”
- Layout:
  - Fundo branco, texto em cinza escuro.
  - Título destacado em verde primário.
  - Espaçamento generoso acima/abaixo.
- Status estrutural e visual: `STATUS_REFINADO`  
- Texto exato do subtítulo e rótulos de chips: `STATUS_AGUARDANDO_REQUISITOS`

### 3.3. Navegação Interna (Âncoras)

- Elemento `nav` no início do corpo, logo após o hero, com `aria-label="Navegação da disciplina"`.
- Conteúdo: lista simples (idealmente `ul`) com links de texto para:
  - Aula 1
  - Aula 2
  - Aula 3
  - Aula 4
  - Aula 5
  - Simulado
- Cada item aponta para um `id` correspondente em seções abaixo, por ex.:
  - `#aula-1`
  - `#aula-2`
  - `#aula-3`
  - `#aula-4`
  - `#aula-5`
  - `#simulado`
- As seções principais devem ser navegáveis a partir do topo e, ao chegar na âncora, o bloco colapsável correspondente deve estar claramente identificado para o aluno expandir o conteúdo desejado.
- Visual:
  - Lista vertical simples (para não parecer menu complexo).
  - Links com bom espaçamento vertical, cores discretas, sublinhado ou mudança visual clara no hover/foco.
- Status estrutural e visual: `STATUS_REFINADO`  
- Textos exatos dos rótulos (se quiser frases mais longas que “Aula 1”, etc.): `STATUS_AGUARDANDO_REQUISITOS`

### 3.4. Seção Aula 1 – Estrutura

- Elemento `section` com `id="aula-1"`.
- Hierarquia:
  - `h2`: “Aula 1 – IA para Geração de Código: Do Prompt ao Pull Request Profissional”.
  - Parágrafo introdutório curto explicando objetivo da aula: introduzir como a intenção humana se traduz em software com IA, do contexto ao fluxo profissional de entrega.
  - Subsecao de materiais adicionais no topo da aula.
  - Mini sumário interno (opcional): lista simples de links para cada tópico da Aula 1 (âncoras locais).
  - Subsecao de links úteis ao final da aula.
- Status estrutural: `STATUS_REFINADO`  
- Texto do parágrafo introdutório: `STATUS_REFINADO`

#### 3.4.1. Materiais adicionais (Aula 1)

- Subsecao no topo da aula com `h3`: “Materiais adicionais”.
- Lista (`ul`) com links clicáveis:
  - [Apresentação (Slides)](https://docs.google.com/presentation/d/1kob3cR_TYodHgQjRqc5xoCXT85kw2PmuNwb6aJG7Ivo/edit?slide=id.p15#slide=id.p15)
  - [Repositorio no GitHub](https://github.com/Luanes/lab365-luane-lazuli)
- Status estrutural e visual: `STATUS_REFINADO`
- Lista final de materiais (Aula 1): `STATUS_REFINADO`

#### 3.4.2. Mini Sumário da Aula 1 (Opcional)

- Conteúdo em lista (por exemplo, `ul`):
  - Link para tópico 1: “Fundamentos Filosóficos: Evolução da Inteligência e Intenção”
  - Link para tópico 2: “A Interface de Comunicação: Contexto e Prompt”
  - Link para tópico 3: “Engenharia de Prompt e o Colapso do Contexto”
  - Link para tópico 4: “A Quebra de Intenção na Geração de Aplicações”
  - Link para tópico 5: “Vibe Coding vs. Spec-Driven Development (SDD)”
  - Link para tópico 6: “O Fluxo de Trabalho: Do Prompt ao PR”
- Cada link aponta para cards abaixo, com ids como:
  - `#topico-1-1`, `#topico-1-2`, …, `#topico-1-6`
- Status estrutural: `STATUS_REFINADO`  
- Conteúdos internos (textos descritivos dentro de cada tópico): `STATUS_REFINADO`

#### 3.4.3. Cards dos 6 Tópicos da Aula 1

Para cada tópico:

1. **Tópico 1 – “Fundamentos Filosóficos: Evolução da Inteligência e Intenção”**  
2. **Tópico 2 – “A Interface de Comunicação: Contexto e Prompt”**  
3. **Tópico 3 – “Engenharia de Prompt e o Colapso do Contexto”**  
4. **Tópico 4 – “A Quebra de Intenção na Geração de Aplicações”**  
5. **Tópico 5 – “Vibe Coding vs. Spec-Driven Development (SDD)”**  
6. **Tópico 6 – “O Fluxo de Trabalho: Do Prompt ao PR”**

- Estrutura de cada card:
  - `article` ou `div` com classe comum (ex.: card-topico) e `id` correspondente (`topico-1-1`, etc.).
  - `h3` com o título do tópico.
  - Conteúdo completo do tópico (parágrafos, listas e citações), conforme abaixo.
- Visual:
  - Fundo branco.
  - Borda fina cinza clara e cantos levemente arredondados.
  - Título em verde primário, texto em cinza escuro.
  - Espaçamento interno confortável (padding) e margem entre cards.
- Status da estrutura e visual dos cards: `STATUS_REFINADO`  
- Conteúdo pedagógico (texto completo de cada tópico): `STATUS_REFINADO`

##### Conteúdo completo por tópico

**Tópico 1 – Fundamentos Filosóficos: Evolução da Inteligência e Intenção** (`#topico-1-1`)

- Parágrafo de abertura: A reflexão sobre máquinas que "pensam" acompanha a fundação da ciência da computação. Para traduzir intenção humana em software funcional, é preciso compreender como a relação com a computação se estabeleceu.
- Subtítulo ou destaque em negrito: "A Evolução da Inteligência (Alan Turing)".
- Citação em bloco: "Não poderiam as maquinas realizar algo que devesse ser chamado de pensar, ainda que muito diferente do que faz um ser humano?"
- Parágrafo: A definição de "inteligência" mudou ao longo da filosofia, assim como a definição médica do que é estar "vivo". Ainda que a IA não seja uma inteligência por natureza, ela possui mecanismos lógicos sofisticados; a base teórica de Turing já reconhecia essa capacidade.
- Subtítulo ou destaque em negrito: "Interpretação vs. Descoberta (John Searle)".
- Citação em bloco: "Você não pode descobrir que o cérebro é um computador digital, só pode interpretar o cérebro como um computador digital."
- Parágrafo: Não descobrimos que o cérebro é uma máquina; interpretamos assim para facilitar a compreensão. Esse mecanismo computacional foi desenvolvido por humanos, que digitalizaram essas operações para simular uma "inteligência" artificial.
- Subtítulo ou destaque em negrito: "O Ponto de Partida: O Contexto".
- Parágrafo: A digitalização da nossa compreensão do mundo é a chave para construir e operar sistemas inteligentes. Engenharia de software com IA não começa com código aleatório, mas com contexto, pois é ele que transmite intenção e interpretação do mundo para a máquina.

**Tópico 2 – A Interface de Comunicação: Contexto e Prompt** (`#topico-1-2`)

- Parágrafo de abertura: A IA, especialmente os Grandes Modelos de Linguagem (LLMs), atua por meio de mensagens. O "L" de LLM significa Linguagem.
- Subtítulo ou destaque em negrito: "O que é o Contexto na Prática?".
- Parágrafo: Contexto é o conjunto de informações de entrada que o modelo usa para interpretar a requisição e gerar uma resposta adequada.
- Lista com as quatro vantagens do contexto:
  - Instruções de Sistema: diretrizes de base que definem papel e comportamento da IA.
  - Arquivos: documentos, PDFs, apresentações, imagens ou vídeos que expandem a base de conhecimento.
  - Histórico: prompts e respostas anteriores concatenados.
  - Prompt Atual: a entrada imediata e direta do usuário.
- Nota técnica (parágrafo curto): Tecnologias como RAG, Tools e MCP são estratégias para adicionar mais contexto, ajudando a IA a definir melhor seu papel e gerar respostas mais precisas.
- Subtítulo ou destaque em negrito: "O que é o Prompt?".
- Parágrafo: O prompt é a interface principal da IA e traduz a intenção humana, combinada ao contexto para definir a resposta final da máquina.

**Tópico 3 – Engenharia de Prompt e o Colapso do Contexto** (`#topico-1-3`)

- Parágrafo de abertura: Para entender falhas de comunicação com a IA, é preciso compreender como ela constrói respostas.
- Subtítulo ou destaque em negrito: "Como a IA gera respostas: A Previsão de Tokens".
- Parágrafo: LLMs são modelos estatísticos preditivos; sua função é prever o próximo token. A cada instante, a IA calcula o token mais provável com base em duas fontes.
- Lista das duas fontes:
  - Todo o contexto fornecido (instruções de sistema, arquivos, histórico e prompt atual).
  - O próprio texto já gerado na resposta.
- Subtítulo ou destaque em negrito: "A Matemática do Contexto e a Redução de Alucinações".
- Parágrafo: Quanto melhor a definição do contexto e do objetivo do agente, mais se afunilam as probabilidades do modelo. Regras claras e persona específica trazem padrões e jargoes do dominio, aumentando a aderencia das respostas.
- Parágrafo: Quando o usuario nao traduz a intencao em um prompt claro, ocorre o Colapso do Contexto (quebra da intencao original). A IA responde literalmente ao que foi pedido.
- Subtítulo ou destaque em negrito: "Exemplos Praticos do Colapso".
- Lista de exemplos:
  - Cacto-Tomate: o usuario pediu "um cacto com forma de tomate" e a IA gerou um tomate com um cacto em cima, atendendo literalmente a instrucao.
  - Tsunami com Cara Feliz: ao tentar refinar um tsunami para ter rosto feliz, a IA gerou monstros e ondas com olhos gigantes, mostrando como instrucoes ambiguas degradam o resultado.
- Parágrafo: Para evitar isso, usa-se Engenharia de Prompt para escopar o universo de opcoes da IA.
- Subtítulo ou destaque em negrito: "Tecnica 1: Role Prompting".
- Parágrafo: A IA assume uma persona profissional, acessando um subconjunto especifico de dados do treinamento.
- Exemplo em bloco de texto:
  - "Aja como um Web Designer Senior especializado em EdTech. Sua missao e criar o codigo HTML de um componente de 'Plano de Aulas'..."
- Parágrafo: Vantagem: a IA adota tom de voz, jargoes e premissas da area, eliminando explicacoes basicas e gerando tokens mais aderentes ao dominio.
- Subtítulo ou destaque em negrito: "Tecnica 2: Framework P.A.C.I.F.".
- Parágrafo: Funciona como um formulario para garantir completude.
- Lista P.A.C.I.F.:
  - P - Papel (Persona): Você e um Especialista em Web Design com foco em UX...
  - A - Acao (Tarefa): Crie o codigo HTML para uma secao de 'Plano de Aulas'...
  - C - Contexto: Para ser inserida em um Google Site voltada para alunos do curso 'IA para Devs'.
  - I - Instrucoes: Layout limpo. Estrutura com titulo e 3 cartoes semanais. Use tons de azul e cinza.
  - F - Formato: Entregue apenas o codigo HTML puro, pronto para copiar e colar.

**Tópico 4 – A Quebra de Intenção na Geração de Aplicações** (`#topico-1-4`)

- Parágrafo de abertura: Ao construir software de forma iterativa com IA, o acúmulo e o excesso de contexto podem virar inimigos.
- Subtítulo ou destaque em negrito: "O Caso Real da Pagina Web".
- Lista de etapas do caso real:
  - O Inicio: o usuario pediu uma pagina de "IA para Devs" com React e Tailwind. (Sucesso)
  - A Adaptacao: pediu para alterar para um arquivo .html estatico, compativel com Google Sites. (Sucesso)
  - A Nova Feature: solicitou uma nova secao de simulado.
- Subtítulo ou destaque em negrito: "O Problema".
- Parágrafo: A IA gerou o simulado, mas apagou menu e secoes anteriores.
- Subtítulo ou destaque em negrito: "A Causa: O Limite da Janela de Contexto".
- Parágrafo: O historico cresceu e estourou a janela de contexto da LLM. Ao processar a nova instrucao, a IA esqueceu componentes originais, quebrando a intencao e a integridade do software.

**Tópico 5 – Vibe Coding vs. Spec-Driven Development (SDD)** (`#topico-1-5`)

- Parágrafo de abertura: Para evitar a quebra de intencao, e preciso mudar a forma de construir software com IA.
- Subtítulo ou destaque em negrito: "Vibe Coding (O 'Go Horse' da IA)".
- Parágrafo: Pratica de pedidos sequenciais e desestruturados via chat (ex: "Muda a cor", "Tira o menu").
- Parágrafo: Problema: dilui o contexto geral rapidamente. Bom para prototipacao, ruim para manter qualidade no longo prazo, causando alucinacoes e perda de controle.
- Subtítulo ou destaque em negrito: "Spec-Driven Development (O Rigor da Engenharia)".
- Parágrafo: Uso de uma especificacao (SPEC.md) como unica fonte da verdade.
- Parágrafo: Na pratica, o desenvolvedor altera a Spec e instrui a IA a atualizar o codigo com base nela, mantendo foco nos requisitos.
- Subtítulo ou destaque em negrito: "4 vantagens do SDD".
- Lista das vantagens:
  - Portabilidade: a Spec independe da ferramenta.
  - Consistencia: mudanca de regra de negocio passa pela Spec; testes validam a Spec.
  - Empoderamento: permite criar solucoes em stacks nao dominadas profundamente.
  - Rastreabilidade: a Spec documenta o porquê; a IA entrega o como.

**Tópico 6 – O Fluxo de Trabalho: Do Prompt ao PR** (`#topico-1-6`)

- Parágrafo de abertura: A engenharia de software com IA documenta todo o processo de desenvolvimento, unindo Spec e ferramentas classicas para um fluxo profissional e seguro.
- Subtítulo ou destaque em negrito: "O Poder do Git no SDD".
- Parágrafo: Com a Spec como unica fonte da verdade, o Git registra claramente alteracoes de regras de negocio e codigo, facilitando reversoes e PRs robustos.
- Subtítulo ou destaque em negrito: "Resumo da Jornada: As 4 Etapas".
- Lista das 4 etapas:
  - Filosofia (A Intencao): o porquê do projeto e a visao de valorizar a capacidade intelectual humana.
  - Contexto (A Ideacao): fase de experimentacao e uso de Vibe Coding para extrair requisitos.
  - Engenharia (O Rigor): aplicacao do SDD e uso de fluxos de agentes sobre a Spec.
  - Aplicacao (O Produto): entrega final de software previsivel e alinhado a especificacao.

#### 3.4.4. Links úteis (Aula 1)

- Subsecao ao final da aula com `h3`: “Links úteis”.
- Lista (`ul`) com links clicáveis:
  - [Artigo: Role Prompting](https://rediminds.com/future-edge/how-meta-prompting-and-role-engineering-are-unlocking-the-next-generation-of-ai-agents/)
  - [Artigo: P.A.C.I.F](https://www.dio.me/articles/o-guia-definitivo-da-engenharia-de-prompts-uma-jornada-desvendando-o-poder-de-prompts-assertivos)
  - [Artigo: Vibe coding](https://medium.com/@addyosmani/vibe-coding-is-not-the-same-as-ai-assisted-engineering-3f81088d5b98)
  - [Artigo: Spec-Driven Development](https://www.thoughtworks.com/pt-br/insights/blog/agile-engineering-practices/spec-driven-development-unpacking-2025-new-engineering-practices)
  - [Video: Comparacao Spec-driven Development e vibe coding](https://www.youtube.com/watch?v=mViFYTwWvcM)
  - [Artigo: Context Engineering](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)
- Status estrutural e visual: `STATUS_REFINADO`
- Lista final de links úteis (Aula 1): `STATUS_REFINADO`

### 3.5. Seções das Aulas 2 a 5

Para cada aula:

- `section` com ids: `aula-2`, `aula-3`, `aula-4`, `aula-5`.
- Conteúdo:
  - `h2` com título completo da aula:
    - Aula 2 – Construindo um Workflow de Testes Unitários Automáticos com IA
    - Aula 3 – Documentação Viva com IA: Automação, Versionamento e Consistência
    - Aula 4 – Integração de Agentes ao Ecossistema: APIs, RAG e Observabilidade
    - Aula 5 – Arquitetura de Sistemas com IA: Orquestração de Agentes, Memória e Segurança
  - Subsecao de materiais adicionais no topo de cada aula, com `h3` e lista placeholder:
    - “Material adicional 1 – será definido pelo professor.”
  - Um único parágrafo curto, por exemplo:
    - “Conteúdo desta aula será disponibilizado em breve.”
  - Subsecao de links úteis ao final de cada aula, com `h3` e lista placeholder:
    - “Link útil 1 – será definido pelo professor.”
- Visual:
  - Estrutura semelhante: bloco com margem superior, título destacado e texto centralizado ou alinhado à esquerda.
  - Nada além do parágrafo “Em breve” para evitar ruído.
- Status estrutural e visual: `STATUS_REFINADO`  
- Eventuais descrições adicionais futuras de cada aula: `STATUS_AGUARDANDO_REQUISITOS`
### 3.6. Seção “Simulado”

- `section` com `id="simulado"`.
- Conteúdo:
  - `h2`: “Simulado”.
  - Parágrafo explicativo:
    - “Aqui serão disponibilizados os links para simulados e questionários da disciplina.”
  - Lista (`ul`) preparada para receber itens:
    - “Simulado 1 – link será adicionado pelo professor.”
- Status estrutural e visual: `STATUS_REFINADO`  
- Links reais de simulados e descrições: `STATUS_AGUARDANDO_REQUISITOS`

### 3.7. Rodapé Simples

- Pequeno bloco final:
  - Parágrafo discreto:
    - “Página de apoio à disciplina IA para Desenvolvedores – versão inicial.”
  - Opcional: botão “Voltar ao início” com `scrollTo` via JavaScript, evitando ancoras em embeds.
- Status: `STATUS_REFINADO`

---

## 4. Design System e Estilo Visual

### 4.1. Paleta de Cores (inspirada na trilha IA para DEVs)

- Primária:
  - Verde escuro (aprox. `#306719`) para:
    - Títulos principais (`h1`, `h2`).
    - Destaques e futuros botões/CTAs (se vierem a ser usados).
- Secundárias / neutras:
  - Texto: cinza escuro (ex.: `#333333` ou próximo).
  - Texto secundário: cinza médio (ex.: `#555555`).
  - Bordas e divisores: cinza claro (ex.: `#DDDDDD` ou `#BBBBBB`).
- Fundo:
  - Branco (`#FFFFFF`) predominante.
  - Pode-se usar um cinza muito claro em faixas específicas, se necessário, sem poluir visualmente.
- Status: `STATUS_REFINADO`

### 4.2. Tipografia

- Fonte base:
  - `font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;`
- Tamanhos (referenciais):
  - Corpo de texto: ~16px.
  - `h1`: significativamente maior (≈ 32px).
  - `h2`: entre 24–28px.
  - `h3`: entre 18–20px.
- Peso:
  - Títulos em negrito.
  - Corpo de texto em peso normal.
- Status: `STATUS_REFINADO`

### 4.3. Layout e Espaçamento

- Coluna única:
  - Largura máxima do conteúdo centralizado ~800px.
  - Margens laterais em mobile preenchendo quase toda a largura, mas mantendo margens mínimas.
- Espaçamento:
  - Margem vertical generosa entre seções.
  - Padding interno em cards da Aula 1 para legibilidade.
- Elementos gráficos:
  - Sem ícones decorativos, imagens ou vídeos nesta página, para manter foco no conteúdo escrito.
- Status: `STATUS_REFINADO`

---

## 5. Acessibilidade e Experiência do Aluno

### 5.1. Estrutura Semântica

- Um único `h1` (título da página).
- `h2` para seções principais (Aulas 1–5, Simulado).
- `h3` para subtópicos da Aula 1 e subsecoes de materiais/links das aulas.
- Uso de `nav` com `aria-label="Navegação da disciplina"`.
- Status: `STATUS_REFINADO`

### 5.2. Navegação e Foco

- Links de navegação interna claramente identificáveis, com foco visível (outline padrão mantido).
- Ordem lógica de tabulação seguindo a ordem visual da página.
- Status: `STATUS_REFINADO`

### 5.3. Contraste e Leitura

- Contraste entre texto e fundo atendendo nível AA mínimo.
- Altura de linha ≥ 1.5 para textos.
- Parágrafos curtos, evitando blocos grandes de texto.
- Status: `STATUS_REFINADO`

### 5.4. Conteúdos Pendentes do Professor

- Descrições de Aulas 2–5 (se houver interesse em expandir além de “Em breve”).
- URLs e descrições de materiais adicionais e links úteis das Aulas 2–5.
- Links reais de simulados / questionários.
- Todos estes permanecem com status: `STATUS_AGUARDANDO_REQUISITOS`

---

## 6. Resumo dos Itens por Status

- `STATUS_REFINADO` (pronto para desenvolvimento):
  - Estrutura HTML global (head, body, seção única centralizada).
  - Header/hero da disciplina (estrutura e estilo).
  - Navegação interna por âncoras (estrutura e estilo).
  - Seção Aula 1: estrutura, materiais adicionais (com links reais), mini sumário, cards dos 6 tópicos e links úteis (com links reais).
  - Seções Aulas 2–5 com mensagem “Em breve”, materiais adicionais e links úteis como placeholders internos.
  - Seção “Simulado” (estrutura de lista com placeholders).
  - Rodapé simples.
  - Paleta de cores, tipografia e layout base.
  - Diretrizes de acessibilidade (hierarquia de headings, nav, foco, contraste).

- `STATUS_AGUARDANDO_REQUISITOS` (depende de definições suas):
  - Textos definitivos:
    - Subtítulo do header.
    - Eventuais descrições complementares de Aulas 2–5 (caso queira mais do que “Em breve”).
  - URLs e rótulos finais:
    - Materiais adicionais e links úteis das Aulas 2–5.
    - Simulados / questionários.
