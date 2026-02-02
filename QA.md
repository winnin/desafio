# Desafio Técnico – Quality Assurance (QA) | Winnin

## Objetivo

Avaliar a capacidade do candidato em **planejar, modelar e automatizar testes** de ponta a ponta (E2E) e de API, aplicando boas práticas de qualidade, organização, clareza de critérios de aceite e automação, utilizando preferencialmente o **Playwright**.

O desafio é composto por **duas partes complementares**, que devem coexistir no **mesmo repositório**:

1. Modelagem de cenários em BDD + Automação de testes E2E  
2. Automação de testes de API  

---

## Estrutura Geral do Projeto

O repositório deve conter:

- Testes E2E baseados em BDD
- Testes automatizados de API
- Estrutura organizada de pastas
- README com instruções claras de execução

---

## Parte 1 – BDD + Automação de Testes E2E

### Contexto

O site **ge.globo.com** exibe notícias esportivas organizadas por esportes, campeonatos e clubes. A página inicial destaca as principais manchetes e permite navegação para páginas específicas de times.

O candidato deverá:

- Modelar critérios de aceite utilizando **BDD (Gherkin)**
- Utilizar esses critérios como base para a automação dos testes E2E
- Implementar os testes utilizando **Playwright**

---

### Regra de Negócio

- O site deve exibir as últimas notícias esportivas
- As principais manchetes devem aparecer em destaque na página inicial
- Cada notícia deve conter:
  - Título
  - Imagem destacada
  - Resumo
  - Link para a matéria completa

---

### Critérios de Aceite (BDD)

Os critérios devem ser escritos em **BDD (Gherkin)** e podem ser incluídos no próprio `README.md` ou em arquivos `.feature`.

Critérios mínimos obrigatórios:

- A página inicial deve exibir no mínimo **10 notícias**
- Cada notícia deve conter:
  - Título
  - Imagem destacada
  - Resumo
- Ao clicar em uma notícia, o usuário deve ser redirecionado para a matéria completa
- Ao selecionar um time da **Série A do Campeonato Brasileiro**, o usuário deve ser redirecionado para a página do clube, onde poderá visualizar notícias relacionadas

---

### Automação E2E – Requisitos Técnicos

- Utilizar **Playwright**
- Implementar **Page Object Model**
- Adotar boas práticas de código e organização
- Garantir que os testes executem sem falhas
- Código limpo, legível e bem estruturado

---

## Parte 2 – Automação de Testes de API

### Contexto

Utilizar a **API pública ServeRest (serverest.dev)**, que simula um e-commerce com os seguintes recursos:

- Usuários
- Login
- Produtos
- Carrinhos

O objetivo é avaliar a capacidade de **planejar, implementar e manter uma suíte de testes automatizados de API**, com boas práticas de engenharia de testes.

---

### Setup

- Recomenda-se executar a ServeRest **localmente**, por exemplo:
  - `npx serverest@latest`
  - Docker (conforme documentação oficial)
  - Caso utilize o ambiente público, explicar no `README.md`:
  - Estratégia para evitar flakiness
  - Geração de dados únicos (ex.: e-mails)

---

### Requisitos Mínimos de Testes

Os testes **devem criar seus próprios dados**, não dependendo de massa pré-existente.

#### Usuários (`/usuarios`)

- Criar usuário com sucesso (status `201`)
- Validar:
  - Status code
  - Campos essenciais no body
  - Coerência dos valores
- Erros (mínimo 2): Email inválido
  - Campo `administrador` fora de `true/false`
  - Campo obrigatório ausente (opcional como extra)

---

#### Login (`/login`)

- Realizar login com sucesso utilizando o usuário criado
- Capturar token (quando aplicável)
- Erro (mínimo 1):Login com senha incorreta (validar mensagem e estrutura de erro)

---

#### Produtos (`/produtos`)

- Criar produto com sucesso utilizando credenciais adequadas  
  (ex.: usuário administrador + token)
- Validar contrato do produto criado:
  - Campos
  - Tipos
  - Valores
- Erro (mínimo 1):Criar produto com preço inválido (negativo ou não-inteiro)

---

#### Carrinhos (`/carrinhos`)

- Criar carrinho com sucesso contendo o produto criado anteriormente
- Validar:
- `idProduto`
- Quantidade
- Erro (mínimo 1): Quantidade menor ou igual a zero

---

## Requisitos de Qualidade (Avaliação Geral)

Serão avaliados:

- Organização e estrutura do projeto
- Boas práticas de automação
- Isolamento e independência dos testes
- Estratégia de limpeza de dados (cleanup), quando aplicável
- Clareza dos cenários e validações
- Legibilidade e manutenibilidade do código

---

## Pontos Extras (Não Obrigatórios)

- Execução dos testes via **GitHub Actions** (`workflow_dispatch`)
- Uso de variáveis de ambiente
- Separação clara entre testes E2E e API
- Uso de fixtures e helpers reutilizáveis

---

## Entregáveis

- Repositório Git público
- Código-fonte completo
- `README.md` contendo:
  - Instruções de execução
  - Dependências do projeto
  - Estratégias adotadas (especialmente para testes de API)

---

Boa sorte! 

