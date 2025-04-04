# Desafio Quality Assurance

Resumo do Desafio
O objetivo deste desafio é avaliar a capacidade do candidato em modelar critérios de aceite em BDD para as funcionalidades do site [ge.globo.com](https://ge.globo.com/). Esses critérios devem servir como base para a criação de testes automatizados utilizando o framework Playwright.

## Critérios Técnicos Avaliados:
* Implementação da estrutura com Page Object
* Adoção de boas práticas de código e organização
* Clareza na modelagem dos criterios de aceite para BDD
* Execução dos testes sem falhas
* Commits organizados no Git
* Conhecimento da ferramenta Playwright

Pontos extras:
* Implementar a execução dos testes como `workflow_dispatch` no Github Actions;

## Regra de Negócio:
O site deve exibir as últimas notícias esportivas, organizadas por esportes e competições. As manchetes principais devem ficar em destaque na página inicial. Cada notícia deve conter: Título, Imagem destacada, Resumo, Link para a matéria completa

## Critérios de Aceite
1. A página inicial deve exibir no mínimo 10 notícias.
2. Cada notícia deve conter um título, uma imagem destacada e um resumo.
3. Ao clicar em uma notícia, o usuário deve ser redirecionado para a matéria completa.
4. Ao selecionar um time da Série A do Campeonato Brasileiro, o usuário deve ser redirecionado para a página do clube, onde poderá visualizar notícias relacionadas a ele.


Obs: A modelagem do BDD pode ser escrita no README do desafio junto com as infos das dependências do projeto. 

Boa sorte!







