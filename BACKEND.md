# Desafio Backend - Sistema de Pedidos

## Introdução

A empresa _fictícia_ está crescendo rapidamente e precisa de uma API eficiente para gerenciar seus pedidos. Eles querem uma solução moderna, usando GraphQL, e precisam garantir que o banco de dados seja otimizado para consultas rápidas e seguras. Seu desafio é construir essa API!

Você precisa criar uma API que permita:

- Cadastrar usuários, listar usuários e seus pedidos, cadastrar produtos, listar produtos e emitir ordens de compra de produtos.
- O sistema deve garantir que pedidos simultâneos sejam processados corretamente, mantendo a integridade do estoque. Se um pedido não puder ser concluído por falta de estoque, deve ser rejeitado com um erro apropriado.
- Disponibilizar a API via GraphQL.
- Dockerfile com um docker-compose para rodar o projeto
- configurar um workflow no GitHub Actions (opcional)
- API escrita preferencialmente em Nodejs ou Golang

Você será avaliado:

- Nas decisões técnica adotadas para realização do desafio
- Performance da API
- Conhecimentos arquiteturais

## Entrega

- Um repositório com a API implementada
- Documentação explicando as decisões técnicas.

## Sugestão de estrura

Aqui tem um direcionamento de estrutura para realização do desafio, lembrando que isso é só uma sugestão, fica a cargo de você decidir o que é melhor.

```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    created_at TIMESTAMP DEFAULT NOW()
);

CREATE TABLE products (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    price DECIMAL(10,2) NOT NULL,
    stock INT NOT NULL,
    created_at TIMESTAMP DEFAULT NOW()
);

CREATE TABLE orders (
    id SERIAL PRIMARY KEY,
    user_id INT REFERENCES users(id),
    total DECIMAL(10,2) NOT NULL,
    created_at TIMESTAMP DEFAULT NOW()
);

CREATE TABLE order_items (
    id SERIAL PRIMARY KEY,
    order_id INT REFERENCES orders(id),
    product_id INT REFERENCES products(id),
    quantity INT NOT NULL,
    price DECIMAL(10,2) NOT NULL
);
```
