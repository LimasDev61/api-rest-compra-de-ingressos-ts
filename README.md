# api-rest-compra-de-ingressos-ts
 Este diretório contém um estudo de API REST com conceitos de banco de dados local.

# Desafio de API REST

# Primeiros passos para utilizar meu código para teste:

1. Clone o projeto
2. Use o comando `npm install` para instalar as dependências
3. A porta configurada para sua aplicação rodar é a 3000. Caso deseje trocá-la, mude o valor da variável "PORTA" que está dentro do arquivo ".env"
4. Use o comando `npm run dev` para rodar o projeto
5. Aconselho utilizar o Postman insomnia para acessar as rotas da API-REST

## Descrição do desafio

Você acabou de ser contratado pela melhor empresa de tecnologia do mundo: a **CUBOS**.

Sua primeira tarefa como desenvolvedor é criar uma API para um site de compra de ingressos para eventos. Esse será um projeto **piloto**, ou seja, no futuro outras funcionalidades serão implementadas.

Seu papel é construir uma API RESTful que permita ao usuário:

- Listar os eventos cadastrados
- Criar uma conta
- Fazer login
- Fazer uma compra
- Listar compras
- Cancelar uma compra

## rotas de acesso do código:

### `GET /` :
Inicia o servidor com a frase "API de vendas de ingressos".

### `GET` `/eventos?maxPreco=5000` :
Esse endpoint deverá listar todos os eventos cadastrados no banco. Caso o filtro maxPreco seja passado, deverá mostrar somente os eventos com preço menor ou igual ao filtro.

### `POST` `/usuarios`:
Esse endpoint deverá cadastrar um novo usuário no sistema.

### `POST` `/login`:
Esse endpoint será responsável pelo login do usuário.

## Todos os endpoints à partir deste ponto precisam que a validação do envio do comprovante de login seja feita, e que esse comprovante será passado como parâmetro de consulta (query).

### `POST` `/compras?comprovante=COMPROVANTE_LOGIN`:
Essa rota será responsável pela criação de uma nova compra.

### `GET` `/compras?comprovante=COMPROVANTE_LOGIN`:
Essa rota será responsável pela listagem das compras de um usuário.

### `DELETE` `/compras/:id?comprovante=COMPROVANTE_LOGIN`:
Essa rota será responsável por cancelar uma compras de um usuário.



