# Portfólio — Leonardo Beranger Gomes

Portfólio pessoal em estética cyberpunk, construído como uma única página (SPA) em HTML, CSS e JavaScript puros — sem frameworks ou build step.

## Sobre

- Descrição do profissional

## Estrutura do site

- **Home** — apresentação, resumo profissional e stack.
- **Experiência** — linha do tempo completa das posições ocupadas.
- **Projetos** — repositórios do GitHub agrupados por categoria (Data Science, Power BI, Python, HTML, IA).
- **Sobre** — perfil detalhado, filosofia de trabalho e tempo de experiência calculado automaticamente a partir da data de início de carreira.
- **Contato** — e-mail, LinkedIn e GitHub.

## Idiomas

O site é trilíngue: português (padrão), inglês e espanhol. O seletor fica no cabeçalho.

- O idioma inicial vem, nesta ordem: do parâmetro `?lang=` na URL, do `localStorage`, do idioma do navegador; se nada casar, cai em português.
- A escolha fica salva no navegador e a URL vira compartilhável — por exemplo `?lang=en#projects` abre a página de projetos em inglês.
- Todo texto traduzível vive no próprio `index.html`, em objetos `{ pt, en, es }` resolvidos pela função `L()`. Para acrescentar um texto novo, adicione a chave em `UI` e marque o elemento com `data-i18n="chave"` (ou `data-i18n-html` quando o texto contiver marcação).

## Tecnologias

- Principais tecnologias utilizadas pelo profissional

## Contato

- Contatos possíveis para o profissional
