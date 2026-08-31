# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Dois públicos de peso igual, que chegam pelo mesmo link e nunca são endereçados separadamente:

1. **Recrutador ou gestor de vaga** avaliando Leonardo Beranger Gomes para posições de analista de dados, analista de BI ou engenharia de dados. Normalmente chega pelo LinkedIn, com pouco tempo, querendo verificar competência técnica rápido.
2. **Empresa com processo manual doendo** (planilha compartilhada, follow-up por e-mail, relatório montado à mão) avaliando se ele resolve o problema. Procura evidência de que o problema dela já foi resolvido antes.

O site não tem seção separada por público: cada peça precisa servir aos dois ao mesmo tempo.

## Product Purpose

Portfólio pessoal de Leonardo Beranger Gomes — analista de dados/BI, formado em Engenharia de Controle e Automação, Green Belt Lean Six Sigma. Existe para converter uma visita curta em uma das quatro coisas, todas contando como sucesso:

- entrar em contato (e-mail ou LinkedIn);
- abrir os projetos no GitHub e ver código real;
- formar uma impressão de competência mesmo sem clicar em nada;
- lembrar dele depois.

As quatro têm peso: o site é prova e funil ao mesmo tempo, não só um índice de links.

## Positioning

A trajetória é o argumento: engenharia de controle e automação industrial → automação de supermercados e eficiência energética → dados. Ele não chega aos dados pela via da análise pura, e sim pela do processo — o que sustenta atravessar o problema inteiro, do processo manual até o dashboard governado, passando por automação, banco e modelagem. O Green Belt Lean Six Sigma é a credencial que nomeia esse olhar. Um portfólio de analista de dados vizinho não copia essa combinação sem ter vivido a mesma migração.

## Operating Context

- Visita curta, quase sempre iniciada em outra aba (LinkedIn, GitHub, currículo enviado por e-mail).
- Tráfego significativo de celular, especialmente vindo do app do LinkedIn.
- Público internacional real: parte dos visitantes lê em inglês ou espanhol.
- O site é a única superfície própria dele; o resto do conteúdo mora em plataformas de terceiros (LinkedIn, GitHub).

## Capabilities and Constraints

- Single-page application em HTML, CSS e JavaScript puros, um único `index.html`, servido por GitHub Pages a partir de `main`. Não há build step hoje — mas isso é o estado atual da implementação, não um compromisso: o usuário deixou explícito que o stack pode mudar se houver bom motivo.
- Cinco telas internas por troca de `data-page`: home, experiência, projetos, sobre, contato.
- Conteúdo (projetos, empregos, filosofia, contatos, proficiência) vive em arrays JavaScript no próprio `index.html`; não há CMS nem fonte de dados externa.
- Trilíngue PT/EN/ES, com detecção por `?lang=`, `localStorage` e idioma do navegador, e URL compartilhável por idioma.
- O tempo de experiência é calculado em runtime a partir de março de 2021; não é um número escrito à mão.
- Sem analytics, sem formulário, sem backend. Contato acontece por `mailto:` e links externos.

## Brand Commitments

- **A estética cyberpunk é vinculante.** Paleta neon sobre fundo `#060126` (teal `#1BF2B5`, pink `#F21D92`, roxo `#E031EB`), tipografia Orbitron + Share Tech Mono, efeitos de CRT, scanline, glitch no nome e rótulos em estilo terminal (`// PORTFOLIO.INIT`). Trabalho futuro refina esse mundo; não o substitui.
- **Os três idiomas são vinculantes.** Toda peça nova de conteúdo nasce em PT, EN e ES.
- Assinatura declarada no próprio site: "este site foi criado por mim" — o portfólio é também demonstração de que ele constrói a própria superfície.
- Nunca se apresentar como júnior. O conteúdo demonstra capacidade; nível se negocia na conversa.

## Evidence on Hand

- 10 repositórios públicos reais, linkados por card: Energy-Prediction, Projeto-Spotfy, Premier-League, gerenciar_workspace_power_bi, email_relatorio, envio_de_email, ferramentas, catholic-day, portfolio, linkedin-aux.
- Cinco posições reais com empresa, período e descrição (Cirion Technologies, act digital, Grupo Luminae Energia ×3).
- Certificação Green Belt Lean Six Sigma; formação no Centro Universitário FEI (2018–2022).
- Contatos verificáveis: e-mail, LinkedIn, GitHub.
- **Não existem, e não devem ser fabricados:** depoimentos, logos de clientes, métricas de resultado, número de usuários, prêmios, screenshots de dashboards corporativos. Os projetos da Cirion não podem aparecer com nome de cliente, sistema interno ou volume real — a mesma regra de anonimização da skill `linkedin-aux`.
- Não há currículo em PDF publicado no site hoje.

## Product Principles

1. **Servir aos dois públicos na mesma peça.** Problema em linguagem de negócio, solução em linguagem técnica concreta. Uma peça que só serve a um dos dois está incompleta.
2. **Prova antes de afirmação.** Cada alegação de competência precisa de um artefato clicável ou de um detalhe técnico que só quem fez saberia. Adjetivo sozinho não conta.
3. **A visita é curta e começa em outra aba.** A primeira tela decide se haverá segunda. Nada que exija scroll para justificar a permanência.
4. **Paridade entre idiomas.** Uma funcionalidade ou conteúdo que existe só em português é uma funcionalidade quebrada para parte do público real.
5. **Nada fabricado.** Sem depoimento, cliente, métrica ou selo inventado — nem como placeholder de layout.

## Accessibility & Inclusion

Não há requisito formal estabelecido pelo usuário. Duas necessidades reais decorrem do contexto: leitura em celular vinda do LinkedIn, e leitores que não dominam português. Os efeitos de CRT, scanline e glitch são decorativos e precisam continuar sendo puramente decorativos para quem usa leitor de tela ou reduz movimento.
