# Desafio Frontend

Você pode usar IA para resolver este desafio, e esse é o nosso jeito de trabalhar, mas não é obrigatório. Se usar, precisa nos mostrar como foi feito e seguir algumas regras, descritas abaixo. O que queremos entender é o seu julgamento: o que você decide, o que questiona e o que rejeita.

## O desafio

Implemente uma aplicação que lista animes de acordo com o [Figma](https://www.figma.com/file/PPvIPPITdlgZo9CeGDVezk/DesafioWinnin?type=design&node-id=3396%3A64&mode=dev).

- ReactJS, com ou sem NextJS, e TypeScript.
- Dados da API [AniList](https://docs.anilist.co/guide/graphql/).
- O usuário pode filtrar por formato e buscar por texto.
- Cada card exibe o `averageScore` com a regra: abaixo de 50, vermelho; de 50 a 80, amarelo; acima de 80, verde.
- É mandatório seguir e reproduzir as informações contidas no Figma.

O enunciado é enxuto de propósito. Parte do que avaliamos é o que você percebe, decide e entrega além do que está escrito aqui.

## Uso de IA

Usar IA é uma escolha sua e não é eliminatório deixar de usar. Como trabalhamos com IA no dia a dia, como você a usa é um dos pontos que avaliamos. Se usar (Claude Code, Cursor, Copilot, ChatGPT etc.), siga estas regras:

- **Conte como usou.** Inclua um `AI_LOG.md` com as ferramentas, como organizou o trabalho e como verificou, corrigiu ou rejeitou o que a IA gerou.
- **Mostre o contexto que deu.** Se usou um arquivo de instruções (`CLAUDE.md`, `AGENTS.md`, `.cursor/rules` ou equivalente), inclua no repositório.
- **Mantenha o histórico real.** Commits legíveis, sem esconder a iteração.
- **Responda pelo que entregou.** Você precisa conseguir explicar cada parte do código na conversa técnica.

Se não usou IA, diga isso no README e explique como trabalhou. Nesse caso, o `AI_LOG.md` não é necessário.

Em qualquer caso, inclua um **`DECISIONS.md`** (ou uma seção no README) com decisões técnicas, trade-offs e o que faria com mais tempo.

## Escopo e prazo

- Você tem **4 dias corridos** para entregar.
- O esforço esperado é de algumas horas, não do prazo inteiro. Prefira fazer menos e muito bem feito.
- Não listamos tudo o que esperamos. Decida o que vale entregar dentro do tempo e registre no `DECISIONS.md` o que fez além do pedido e o que deixou de fora.

## Entrega

- Repositório com o código.
- README com instruções de como executar o projeto e rodar os testes, e as decisões técnicas em `DECISIONS.md` (ou em uma seção equivalente do README); o `AI_LOG.md` é necessário apenas se usou IA.
- Projeto publicado em algum serviço (Vercel, Netlify etc.) é um bônus.

## Como avaliamos

Avaliamos a entrega com régua alta, considerando os critérios abaixo:

- Se atende ao que foi pedido e é fiel ao Figma;
- Arquitetura, organização dos componentes e controle de estado;
- Qualidade de engenharia: robustez, testes e desempenho;
- Qualidade do produto para quem o usa, em qualquer contexto de uso;
- Maturidade: o que você identifica e resolve sem que tenha sido pedido, e se as escolhas são bem justificadas;
- Uso de IA: como conduziu a ferramenta, o que verificou e o que decidiu por conta própria.

## Próxima etapa

Quem avançar faz uma conversa técnica de 30 a 45 minutos, com tela compartilhada. Você vai evoluir o seu próprio projeto com um requisito novo, usando as mesmas ferramentas que usou na entrega (com ou sem IA), e explicar suas escolhas. Não é preciso se preparar além de conhecer bem o que entregou.

Em caso de dúvidas, entre em contato com a pessoa que te passou este desafio.

Boa sorte.
