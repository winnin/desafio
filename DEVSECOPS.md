# Desafio DevSecOps

Você deve implementar uma pipeline para automatizar esta [aplicação](https://github.com/anandhakumarmca/simplebloggerapp-backend), seguindo as regras abaixo:
1. Publique a imagem da aplicação no Docker Hub.
1. Faça a análise estática e dinâmica de código na pipeline.
1. Faça deploy da aplicação com algum Ingress Controller - para ser possível acessar a aplicação - em algum cluster Kubernetes.


## Bonus
+ Crie na AWS, utilizando Terraform, um recurso Lambda que faça uma chamada 'GET' a um endpoint que deve ser recebido como parâmetro.
+ Chame esse recurso Lambda fazendo uma chamada 'GET' para 'google.com' toda vez que a imagem da aplicação for publicada no Docker Hub.

## Entrega
Um repositório público contendo:
+ Todos os arquivos desenvolvidos.
+ A pipeline implementada.

## Critérios de Avaliação
+ Implementação da estrutura.
+ Organização dos componentes.
+ Adoção de boas práticas de código e organização.
+ Conhecimento das tecnologias que compõem a pipeline.
+ Princípios e técnicas de segurança implementados.