# Especificação Técnica – Página “IA para Desenvolvedores” (G‑Sites)

## 1. Visão Geral

Página HTML simples para ser incorporada em um Google Sites, servindo como hub da disciplina **IA para Desenvolvedores**, com:

- Foco em baixa carga cognitiva e clareza para o aluno.
- Visual inspirado na trilha oficial **IA para DEVs – SCTEC**, apenas como referência de cores/estética.
- Conteúdo estrutural completo apenas para a **Aula 1**; demais aulas, links, materiais e simulados entram como placeholders.

---

## 2. Stack e Restrições Técnicas

- HTML5 puro, compatível com incorporação no Google Sites.  
  - Status: `STATUS_REFINADO`
- CSS simples, preferencialmente em `<style>` interno dentro do `<head>` (sem frameworks, sem dependências externas obrigatórias).  
  - Status: `STATUS_REFINADO`
- Nenhum JavaScript obrigatório para funcionamento da página (apenas HTML + CSS).  
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
  - Links úteis
  - Materiais adicionais
  - Simulado
- Cada item aponta para um `id` correspondente em seções abaixo, por ex.:
  - `#aula-1`
  - `#aula-2`
  - `#aula-3`
  - `#aula-4`
  - `#aula-5`
  - `#links-uteis`
  - `#materiais-adicionais`
  - `#simulado`
- Visual:
  - Lista vertical simples (para não parecer menu complexo).
  - Links com bom espaçamento vertical, cores discretas, sublinhado ou mudança visual clara no hover/foco.
- Status estrutural e visual: `STATUS_REFINADO`  
- Textos exatos dos rótulos (se quiser frases mais longas que “Aula 1”, etc.): `STATUS_AGUARDANDO_REQUISITOS`

### 3.4. Seção Aula 1 – Estrutura

- Elemento `section` com `id="aula-1"`.
- Hierarquia:
  - `h2`: “Aula 1 – IA para Geração de Código: Do Prompt ao Pull Request Profissional”.
  - Parágrafo introdutório curto explicando objetivo da aula (placeholder).
  - Mini sumário interno (opcional): lista simples de links para cada tópico da Aula 1 (âncoras locais).
- Status estrutural: `STATUS_REFINADO`  
- Texto do parágrafo introdutório: `STATUS_AGUARDANDO_REQUISITOS`

#### 3.4.1. Mini Sumário da Aula 1 (Opcional)

- Conteúdo em lista (por exemplo, `ul`):
  - Link para tópico 1: “A representação do mundo de forma digital”
  - Link para tópico 2: “O que é o prompt e contexto?”
  - Link para tópico 3: “Ideação e vibe coding”
  - Link para tópico 4: “Spec-Driven Development”
  - Link para tópico 5: “Realizando o seu PR com auxílio de IA”
- Cada link aponta para cards abaixo, com ids como:
  - `#topico-1-1`, `#topico-1-2`, …, `#topico-1-5`
- Status estrutural: `STATUS_REFINADO`  
- Conteúdos internos (textos descritivos dentro de cada tópico): `STATUS_AGUARDANDO_REQUISITOS`

#### 3.4.2. Cards dos 5 Tópicos da Aula 1

Para cada tópico:

1. **Tópico 1 – “A representação do mundo de forma digital”**  
2. **Tópico 2 – “O que é o prompt e contexto?”**  
3. **Tópico 3 – “Ideação e vibe coding”**  
4. **Tópico 4 – “Spec-Driven Development”**  
5. **Tópico 5 – “Realizando o seu PR com auxílio de IA”**

- Estrutura de cada card:
  - `article` ou `div` com classe comum (ex.: card-topico) e `id` correspondente (`topico-1-1`, etc.).
  - `h3` com o título do tópico.
  - Parágrafo placeholder:
    - Ex.: “Conteúdo deste tópico será definido pelo professor.”
  - Opcional: uma lista (`ul`) para pontos-chave, inicialmente com item placeholder:
    - Ex.: “Pontos-chave serão adicionados aqui.”
- Visual:
  - Fundo branco.
  - Borda fina cinza clara e cantos levemente arredondados.
  - Título em verde primário, texto em cinza escuro.
  - Espaçamento interno confortável (padding) e margem entre cards.
- Status da estrutura e visual dos cards: `STATUS_REFINADO`  
- Conteúdo pedagógico (texto real de cada tópico e pontos-chave): `STATUS_AGUARDANDO_REQUISITOS`

### 3.5. Seções das Aulas 2 a 5

Para cada aula:

- `section` com ids: `aula-2`, `aula-3`, `aula-4`, `aula-5`.
- Conteúdo:
  - `h2` com título completo da aula:
    - Aula 2 – Construindo um Workflow de Testes Unitários Automáticos com IA
    - Aula 3 – Documentação Viva com IA: Automação, Versionamento e Consistência
    - Aula 4 – Integração de Agentes ao Ecossistema: APIs, RAG e Observabilidade
    - Aula 5 – Arquitetura de Sistemas com IA: Orquestração de Agentes, Memória e Segurança
  - Um único parágrafo curto, por exemplo:
    - “Conteúdo desta aula será disponibilizado em breve.”
- Visual:
  - Estrutura semelhante: bloco com margem superior, título destacado e texto centralizado ou alinhado à esquerda.
  - Nada além do parágrafo “Em breve” para evitar ruído.
- Status estrutural e visual: `STATUS_REFINADO`  
- Eventuais descrições adicionais futuras de cada aula: `STATUS_AGUARDANDO_REQUISITOS`

### 3.6. Seção “Links úteis”

- `section` com `id="links-uteis"`.
- Conteúdo:
  - `h2`: “Links úteis”.
  - Parágrafo explicativo curto:
    - “Aqui você encontrará links importantes citados nas aulas.”
  - Lista (`ul`) com itens placeholder:
    - “Repositório no GitHub – link será adicionado pelo professor.”
    - “Apresentação da aula no Google Apresentações – link será adicionado pelo professor.”
    - “Outros recursos – serão adicionados pelo professor.”
- Visual:
  - Lista simples, sem ícones pesados; links reais virão depois.
- Status estrutural e visual: `STATUS_REFINADO`  
- URLs reais e textos finais dos links: `STATUS_AGUARDANDO_REQUISITOS`

### 3.7. Seção “Materiais adicionais”

- `section` com `id="materiais-adicionais"`.
- Conteúdo:
  - `h2`: “Materiais adicionais”.
  - Parágrafo explicando o objetivo:
    - “Nesta seção ficarão PDFs, artigos, vídeos e outros materiais complementares.”
  - Lista (`ul`) vazia ou com 1–2 itens placeholder:
    - “Material adicional 1 – será definido pelo professor.”
- Status estrutural e visual: `STATUS_REFINADO`  
- Lista final de materiais e descrições: `STATUS_AGUARDANDO_REQUISITOS`

### 3.8. Seção “Simulado”

- `section` com `id="simulado"`.
- Conteúdo:
  - `h2`: “Simulado”.
  - Parágrafo explicativo:
    - “Aqui serão disponibilizados os links para simulados e questionários da disciplina.”
  - Lista (`ul`) preparada para receber itens:
    - “Simulado 1 – link será adicionado pelo professor.”
- Status estrutural e visual: `STATUS_REFINADO`  
- Links reais de simulados e descrições: `STATUS_AGUARDANDO_REQUISITOS`

### 3.9. Rodapé Simples

- Pequeno bloco final:
  - Parágrafo discreto:
    - “Página de apoio à disciplina IA para Desenvolvedores – versão inicial.”
  - Opcional: link “Voltar ao início” apontando para o topo (`#topo` ou similar).
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
- `h2` para seções principais (Aulas 1–5, Links úteis, Materiais adicionais, Simulado).
- `h3` para subtópicos da Aula 1.
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

- Textos detalhados dos 5 tópicos da Aula 1 (corpos dos cards).
- Descrições de Aulas 2–5 (se houver interesse em expandir além de “Em breve”).
- URLs e descrições de:
  - Repositório GitHub.
  - Apresentações no Google Apresentações.
  - Materiais adicionais (PDFs, artigos, vídeos).
  - Simulados / questionários.
- Todos estes permanecem com status: `STATUS_AGUARDANDO_REQUISITOS`

---

## 6. Resumo dos Itens por Status

- `STATUS_REFINADO` (pronto para desenvolvimento):
  - Estrutura HTML global (head, body, seção única centralizada).
  - Header/hero da disciplina (estrutura e estilo).
  - Navegação interna por âncoras (estrutura e estilo).
  - Seção Aula 1: estrutura, mini sumário, cards dos 5 tópicos (sem conteúdo final).
  - Seções Aulas 2–5 com mensagem “Em breve”.
  - Seção “Links úteis” (estrutura de lista com placeholders).
  - Seção “Materiais adicionais” (estrutura de lista com placeholders).
  - Seção “Simulado” (estrutura de lista com placeholders).
  - Rodapé simples.
  - Paleta de cores, tipografia e layout base.
  - Diretrizes de acessibilidade (hierarquia de headings, nav, foco, contraste).

- `STATUS_AGUARDANDO_REQUISITOS` (depende de definições suas):
  - Textos definitivos:
    - Subtítulo do header.
    - Parágrafo introdutório da Aula 1.
    - Conteúdo detalhado e pontos-chave de cada um dos 5 tópicos da Aula 1.
    - Eventuais descrições complementares de Aulas 2–5 (caso queira mais do que “Em breve”).
  - URLs e rótulos finais:
    - Repositório GitHub.
    - Apresentações no Google Apresentações.
    - Materiais adicionais (PDFs, artigos, vídeos).
    - Simulados / questionários.
