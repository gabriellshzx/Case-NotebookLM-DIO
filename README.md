# Case-NotebookLM-DIO
> Projeto desenvolvido como parte do desafio de projeto da DIO, explorando o uso do NotebookLM como ferramenta de aprendizado aplicado à área de finanças quantitativas.

---

## 🎯 Contexto e Objetivos

### Tema escolhido
**Teoria Moderna de Portfólios (Modern Portfolio Theory — MPT)** com foco na **Curva de Eficiência de Markowitz**, um dos pilares da análise quantitativa de investimentos.

### Por que esse tema?
A teoria desenvolvida por Harry Markowitz em 1952 revolucionou a forma como investidores pensam sobre risco e retorno. Compreender a fronteira eficiente é essencial para qualquer profissional que atue em FP&A, gestão de ativos, wealth management ou análise de investimentos — áreas em constante crescimento no mercado financeiro brasileiro.

### Objetivos de estudo
- Compreender os fundamentos matemáticos e econômicos da Teoria Moderna de Portfólios
- Entender como a Curva de Markowitz (Fronteira Eficiente) é construída e interpretada
- Relacionar os conceitos de risco (volatilidade), retorno esperado e correlação entre ativos
- Explorar as limitações práticas da teoria e suas evoluções (CAPM, SML, índice de Sharpe)
- Desenvolver fluência nos principais conceitos para aplicação em contextos profissionais de FP&A e mercado financeiro

---

## 📚 Curadoria de Fontes

As fontes abaixo foram selecionadas por serem abertas, academicamente sólidas e diretamente relevantes ao tema. Todas foram inseridas no NotebookLM para alimentar o caderno temático.

| # | Título | Tipo | Acesso |
|---|--------|------|--------|
| 1 | **Portfolio Selection** — Harry Markowitz (1952) | Artigo científico (PDF) | [Journal of Finance via JSTOR](https://www.jstor.org/stable/2975974) |
| 2 | **Damodaran on Valuation** — Capítulo sobre risco e retorno | PDF gratuito | [NYU Stern — Damodaran Online](http://pages.stern.nyu.edu/~adamodar/) |
| 3 | **Modern Portfolio Theory and Investment Analysis** — Elton, Gruber et al. (capítulos de acesso livre) | PDF parcial | Google Scholar / ResearchGate |
| 4 | **Apostila de Finanças Quantitativas** — material educacional aberto da CVM | PDF | [investidor.gov.br](https://www.investidor.gov.br) |
| 5 | **An Introduction to Risk and Return** — Brealey, Myers & Allen (trecho de acesso livre) | Web / PDF | [MIT OpenCourseWare](https://ocw.mit.edu) |

> 💡 **Critério de seleção:** priorizou-se fontes primárias (o artigo original de Markowitz), materiais de professores renomados (Damodaran) e conteúdo regulatório brasileiro (CVM), garantindo tanto rigor teórico quanto aplicabilidade local.

---

## 🧪 Engenharia de Prompts e "Cicatrizes"

Esta seção documenta o processo de elaboração dos prompts utilizados no NotebookLM, incluindo variações testadas, dificuldades encontradas e aprendizados.

---

### Prompt 1 — Introdução conceitual

**Objetivo:** obter uma explicação clara e didática do conceito central.

```
O que é a Fronteira Eficiente de Markowitz? Explique como ela é construída,
o que os eixos X e Y representam e qual a sua utilidade prática para um
investidor ou analista financeiro.
```

**Resposta obtida:** O NotebookLM gerou uma explicação estruturada com base no artigo original de Markowitz e no material da CVM, descrevendo o eixo X como desvio-padrão (risco) e o eixo Y como retorno esperado. A resposta incluiu citações diretas das fontes.

**Dificuldade encontrada:** A resposta inicial era muito técnica e matemática. Foi necessário reformular o prompt adicionando o pedido de linguagem acessível.

**Prompt refinado:**
```
O que é a Fronteira Eficiente de Markowitz? Explique como ela é construída,
o que os eixos representam e qual a sua utilidade prática — use linguagem
acessível para quem tem conhecimento intermediário em finanças.
```

---

### Prompt 2 — Relação entre correlação e diversificação

**Objetivo:** entender o papel da correlação entre ativos na construção da carteira.

```
Como a correlação entre ativos afeta a forma da Fronteira Eficiente?
O que acontece com o risco da carteira quando a correlação é +1, -1 ou 0?
Use exemplos numéricos simples se possível.
```

**Resposta obtida:** Boa explicação com os três cenários de correlação. O NotebookLM referenciou o artigo de Markowitz e o material de Elton & Gruber para embasar os exemplos.

**Dificuldade encontrada:** O NotebookLM não gerou os exemplos numéricos automaticamente, pois as fontes não os continham de forma explícita. Solução: reformular pedindo uma explicação qualitativa e depois buscar os números em fonte complementar.

---

### Prompt 3 — Limitações da teoria

**Objetivo:** identificar pontos críticos e limitações práticas do modelo.

```
Quais são as principais críticas e limitações práticas da Teoria de Markowitz?
Como essas limitações foram endereçadas por teorias posteriores como o CAPM?
```

**Resposta obtida:** O modelo listou como limitações: a dependência de dados históricos, a sensibilidade às estimativas de retorno esperado, o problema de otimização com muitos ativos e a hipótese de distribuição normal dos retornos.

**Dificuldade encontrada:** As fontes carregadas abordavam as limitações de forma dispersa. O NotebookLM sintetizou bem, mas misturou críticas de fontes diferentes sem deixar claro a origem de cada ponto. Solução: pedir explicitamente que cada limitação fosse acompanhada da fonte.

**Prompt refinado:**
```
Quais são as principais críticas e limitações práticas da Teoria de Markowitz?
Para cada limitação, indique em qual das fontes carregadas ela é mencionada.
```

---

### Prompt 4 — Glossário

**Objetivo:** gerar um glossário técnico consolidado.

```
Com base em todas as fontes carregadas, crie um glossário com os 15 principais
termos técnicos relacionados à Teoria de Markowitz e à construção de carteiras.
Para cada termo, forneça: definição clara, fórmula quando aplicável e
em qual contexto prático ele é utilizado.
```

**Resposta obtida:** Glossário completo e bem estruturado. Esse foi o prompt com melhor resultado na primeira tentativa.

---

### Prompt 5 — Geração de quiz para revisão

**Objetivo:** criar perguntas de revisão para fixação do conteúdo.

```
Com base nas fontes carregadas, gere 10 perguntas de múltipla escolha sobre
a Teoria de Markowitz, com 4 alternativas cada e indicação da resposta correta.
As perguntas devem variar entre nível básico, intermediário e avançado.
```

**Dificuldade encontrada:** O NotebookLM gerou perguntas repetitivas nas primeiras tentativas. Solução: especificar os subtemas de cada pergunta.

**Prompt refinado:**
```
Gere 10 perguntas de múltipla escolha, sendo: 3 sobre conceitos básicos
(retorno esperado, risco, correlação), 4 sobre a construção da fronteira eficiente
e 3 sobre limitações e extensões do modelo (CAPM, índice de Sharpe).
Inclua 4 alternativas e gabarito comentado para cada.
```

---

## 📖 Miniguia de Estudo — Entrega Final

### 1. Resumo Estruturado

#### O Problema que Markowitz Resolveu
Antes de 1952, investidores selecionavam ativos olhando apenas para o retorno esperado individualmente. Markowitz mostrou matematicamente que o que importa não é o risco de cada ativo isolado, mas a **contribuição de cada ativo para o risco total da carteira** — e essa contribuição depende de como os ativos se movem juntos (correlação).

#### Os Ingredientes do Modelo
Para construir a Fronteira Eficiente, precisamos de três insumos para cada ativo:
1. **Retorno esperado (μ)** — média dos retornos históricos ou projeção
2. **Risco individual (σ)** — desvio-padrão dos retornos
3. **Correlação entre pares de ativos (ρ)** — como os ativos se movem juntos

#### A Fronteira Eficiente
A Fronteira Eficiente é o conjunto de todas as carteiras que, para um determinado nível de risco, oferecem o maior retorno possível — ou equivalentemente, para um determinado retorno, apresentam o menor risco possível.

- **Eixo X:** Risco (desvio-padrão da carteira — σ)
- **Eixo Y:** Retorno esperado da carteira (μ)
- **Ponto de Mínima Variância (MVP):** carteira com o menor risco possível
- **Carteiras abaixo da fronteira:** ineficientes (mesmo risco, menor retorno)

#### O Papel da Correlação
| Correlação (ρ) | Efeito na carteira |
|---|---|
| ρ = +1 | Sem benefício de diversificação |
| 0 < ρ < 1 | Diversificação parcial (caso real) |
| ρ = 0 | Diversificação significativa |
| ρ = -1 | Eliminação total do risco (teórico) |

#### Extensões do Modelo
- **CAPM (Capital Asset Pricing Model):** adiciona um ativo livre de risco à análise e deriva a Linha do Mercado de Capitais (CML)
- **Índice de Sharpe:** mede retorno por unidade de risco — (Retorno − Taxa livre de risco) / σ
- **Security Market Line (SML):** relaciona o retorno esperado ao risco sistemático (Beta)

---

### 2. Glossário de Conceitos

| Termo | Definição | Fórmula / Notação |
|---|---|---|
| **Retorno Esperado** | Média ponderada dos retornos possíveis de um ativo | μ = Σ pᵢ · Rᵢ |
| **Desvio-Padrão (σ)** | Medida de dispersão dos retornos em torno da média — proxy do risco total | σ = √Var(R) |
| **Variância** | Quadrado do desvio-padrão; medida de risco | σ² = E[(R − μ)²] |
| **Covariância** | Medida de como dois ativos se movem juntos | Cov(A,B) = ρ · σ_A · σ_B |
| **Correlação (ρ)** | Covariância normalizada entre -1 e +1 | ρ = Cov(A,B) / (σ_A · σ_B) |
| **Fronteira Eficiente** | Conjunto de carteiras que maximizam retorno para cada nível de risco | Curva no plano (σ, μ) |
| **Carteira de Mínima Variância (MVP)** | Carteira com o menor risco possível dado o universo de ativos | Ponto mais à esquerda da fronteira |
| **Diversificação** | Redução do risco pela combinação de ativos com correlação imperfeita | — |
| **Risco Sistemático** | Risco não diversificável; ligado ao mercado como um todo | Medido pelo Beta (β) |
| **Risco Idiossincrático** | Risco específico de um ativo; eliminável via diversificação | σ² − β²·σ²_mercado |
| **Beta (β)** | Sensibilidade do ativo em relação ao mercado | β = Cov(R_i, R_m) / Var(R_m) |
| **Índice de Sharpe** | Retorno em excesso por unidade de risco total | S = (μ − Rf) / σ |
| **Taxa Livre de Risco (Rf)** | Retorno de ativo sem risco (no Brasil: Selic ou CDI) | — |
| **CML (Capital Market Line)** | Linha que conecta o ativo livre de risco à carteira de mercado | μ = Rf + [(μ_m − Rf)/σ_m] · σ |
| **SML (Security Market Line)** | Relaciona retorno esperado ao Beta de um ativo | μᵢ = Rf + βᵢ · (μ_m − Rf) |

---

### 3. Prompts Reutilizáveis para Revisões Futuras

Estes prompts podem ser usados em revisões sobre o tema em qualquer ferramenta de IA (NotebookLM, ChatGPT, Claude, etc.):

```
# REVISÃO CONCEITUAL BÁSICA
"Explique a diferença entre risco total, risco sistemático e risco
idiossincrático na Teoria de Markowitz. Como cada um deles é tratado
na construção de carteiras?"
```

```
# INTERPRETAÇÃO DE GRÁFICOS
"Dado um gráfico da Fronteira Eficiente de Markowitz, como identifico:
a carteira de mínima variância, a carteira ótima com ativo livre de risco
e carteiras ineficientes? O que cada posição no gráfico significa?"
```

```
# APLICAÇÃO PRÁTICA
"Como um analista de FP&A aplicaria os conceitos de Markowitz na gestão
do caixa corporativo ou na avaliação de projetos de investimento com
diferentes perfis de risco?"
```

```
# CONEXÃO COM CAPM
"Como a Teoria de Markowitz se conecta ao CAPM? Qual o papel da
Capital Market Line (CML) e qual a diferença entre ela e a
Security Market Line (SML)?"
```

```
# CRÍTICA E LIMITAÇÕES
"Quais são os principais problemas práticos ao aplicar a otimização
de Markowitz com dados reais de mercado? Como gestores profissionais
contornam essas limitações?"
```

```
# QUIZ RÁPIDO
"Gere 5 perguntas dissertativas sobre a Fronteira Eficiente de Markowitz
para testar meu entendimento. Após eu responder, avalie e complemente
cada resposta com base nas fontes do caderno."
```

---

## 🛠️ Ferramentas Utilizadas

- **[NotebookLM](https://notebooklm.google.com/)** — Google | Ferramenta de IA para estudo baseado em fontes
- **GitHub** — Controle de versão e publicação do projeto

---

## 👤 Autor

Desenvolvido como projeto de portfólio no contexto do desafio da **DIO (Digital Innovation One)**.

> *"Diversification is the only free lunch in investing."* — Harry Markowitz

---

## 📄 Licença

Este projeto é de uso educacional e está disponível para consulta e adaptação com devida referência ao autor.
