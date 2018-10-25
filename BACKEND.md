# Desafio Backend

A prova consiste em criar um programa que consulte a api do [reddit](https://www.reddit.com/dev/api/) uma vez por dia (deve ser uma tarefa agendada para rodar em um horário específico que você definir).

A sua tarefa diária deve salvar num banco de dados SQL as postagens que estejam HOT do subredit [artificial](https://api.reddit.com/r/artificial/hot).  

Você deve salvar título da postagem, nome do autor, timestamp da criação, número de "ups" e número de comentários, e criar dois endpoints para consulta desses dados (endpoints REST ou usando graphql).

O primeiro endpoint deve receber como parâmetro uma data inicial, uma data final e uma ordem (as ordens possíveis são número de "ups" e número de comentários) e deve retornar as postagens criadas dentro desse range seguindo a ordem estipulada (em ordem decrescente)

O segundo endpoint deve receber como parâmetro uma ordem (as ordens possíveis são número de "ups" e número de comentários) e deve retornar uma lista de usuários seguindo a ordem estipulada (em ordem decrescente)

Você pode utilizar qualquer linguagem para resolver o desafio, mas preferimos que seja em node ou python (essas são as linguagens que utilizamos aqui).

Além disso, não esqueça de incluir instruções sobre como executar o seu projeto.

Em caso de dúvidas entre em contato com a pessoa que te passou este desafio.

Boa sorte.