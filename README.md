# Portfólio — Leonardo Beranger Gomes

Portfólio pessoal em estética cyberpunk, construído como uma única página (SPA) em HTML, CSS e JavaScript puros — sem framework e sem build step. Publicado por GitHub Pages a partir de `main`:

**[leonardo-beranger.github.io/portfolio](https://leonardo-beranger.github.io/portfolio/)**

## Sobre

Leonardo Beranger Gomes — analista de dados e BI, formado em Engenharia de Controle e Automação, Green Belt Lean Six Sigma. O site fala com dois públicos ao mesmo tempo, pelo mesmo link: quem contrata analista de dados, BI ou engenharia de dados, e empresas com processo manual doendo. Cada peça precisa servir aos dois — problema em linguagem de negócio, solução em linguagem técnica.

O contexto de produto que orienta o conteúdo está em [`PRODUCT.md`](PRODUCT.md).

## Estrutura do site

- **Home** — apresentação, dois projetos em forma compacta (prova antes de adjetivo) e as ferramentas por trás deles.
- **Projetos** — os dez repositórios no formato **problema → gargalo → solução → ganho**, agrupados por tipo de problema (automação de processo, BI e governança, modelagem e previsão, web) e não por tecnologia.
- **Experiência** — linha do tempo completa das posições ocupadas.
- **Sobre** — perfil detalhado, filosofia de trabalho e tempo de experiência calculado em runtime a partir da data de início de carreira.
- **Contato** — e-mail, LinkedIn e GitHub. Toda página termina com um bloco de contato.

## Idiomas

O site é trilíngue: português (padrão), inglês e espanhol. O seletor fica no cabeçalho.

- O idioma inicial vem, nesta ordem: do parâmetro `?lang=` na URL, do `localStorage`, do idioma do navegador; se nada casar, cai em português.
- A escolha fica salva no navegador e a URL é compartilhável — `?lang=en#projects` abre a página de projetos em inglês.
- Todo texto traduzível vive no próprio `index.html`, em objetos `{ pt, en, es }` resolvidos pela função `L()`. Para acrescentar um texto novo, adicione a chave em `UI` e marque o elemento com `data-i18n="chave"` (ou `data-i18n-html` quando o texto contiver marcação).

## Decisões de implementação

- **Roteamento.** Cinco views coexistem no DOM e são alternadas por classe. `pushState` cria histórico de verdade (o Back volta uma página em vez de sair do site) e um listener de `popstate` cobre o Back e o deep link por hash em documento já carregado. O fragmento `#main`, alvo do skip link, é ignorado pelo roteador.
- **Peso.** O GIF de fundo tem 10 MB e por isso não é declarado em CSS: entra por JavaScript depois do first paint e apenas nas páginas que o usam. Uma carga direta em `#projects` não o requisita. O resto da página soma cerca de 97 KB.
- **Acessibilidade.** Hierarquia real de headings, skip link, `aria-hidden` nas camadas decorativas, `aria-current` no destino ativo, foco movido na troca de página, anel de foco próprio e um bloco `prefers-reduced-motion` que desliga CRT, scanline, glitch e rolagem suave.
- **Contraste.** O texto secundário tem três níveis tintados a partir do próprio foreground, medindo 10,0:1, 7,3:1 e 5,8:1 sobre o fundo — todos acima de AA. Sobre o GIF, nas páginas que o exibem, os valores caem; é um ponto aberto.
- **Tipografia.** Escala em custom properties (`--t-micro` a `--t-title`), com stack de fallback declarada para Orbitron e Share Tech Mono.

## Avaliação de design

O projeto usa a skill [Impeccable](https://impeccable.style) para revisão. Os snapshots de cada rodada ficam em `.impeccable/critique/`, com pontuação por heurística de Nielsen, veredito de especificidade e problemas priorizados.

| Rodada | Nota |
|---|---|
| 2026-08-31 (inicial) | 17/36 |
| 2026-08-31 (pós-correções) | 21/32 |

## Rodando localmente

Não há dependência nem passo de build. Qualquer servidor estático serve:

```bash
python -m http.server 8000
```

Abrir `http://localhost:8000`. Vale usar um servidor em vez de abrir o arquivo direto: `pushState` e `localStorage` precisam de uma origem real.

## Contato

- E-mail: leonardoberangergomes@gmail.com
- LinkedIn: [leonardo-beranger-gomes](https://www.linkedin.com/in/leonardo-beranger-gomes-a7160a1a0)
- GitHub: [leonardo-beranger](https://github.com/leonardo-beranger)
