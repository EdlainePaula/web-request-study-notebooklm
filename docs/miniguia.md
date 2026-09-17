# 🌐 Miniguia — Do Frontend ao Backend

## Introdução

Este miniguia consolida os principais conceitos estudados durante
a investigação sobre  a comunicação front e backend
em uma aplicação web.

O objetivo é acompanhar o caminho percorrido por uma requisição,
desde uma ação realizada pelo usuário até o processamento pelo servidor
e a apresentação da resposta na interface.

## 🔄 Visão geral do fluxo

Usuário
↓
Frontend
↓
Requisição HTTP
↓
API
↓
Backend
↓
Processamento / Banco de Dados
↓
Resposta HTTP
↓
Frontend
↓
Usuário

## 1. A ação começa no Frontend

A comunicação começa a partir de uma ação interativa do usuário, como
clicar em um botão, enviar um formulário ou solicitar alguma informação.

O frontend captura essa interação, normalmente através do JavaScript,
e prepara a solicitação que será enviada ao servidor.

Quando há dados a serem enviados, eles podem ser representados em JSON,
embora esse não seja o único formato possível.

O cliente também precisa saber qual recurso da API deseja acessar,
utilizando um endereço (URI/endpoint), como `/users`.

---

## 2. A requisição HTTP

Após a ação do usuário, o cliente envia uma requisição utilizando HTTP.

O HTTP é responsável por padronizar a comunicação entre cliente e
servidor. Uma requisição pode conter:

- Método HTTP;
- URI do recurso;
- Cabeçalhos (headers);
- Corpo da requisição (body), quando necessário.

Métodos como GET, POST, PUT e DELETE pertencem ao HTTP e podem ser
utilizados por uma API REST para representar diferentes operações
sobre os recursos.

---

## 3. A API

A API funciona como uma interface de comunicação entre o cliente e
as funcionalidades disponibilizadas pelo backend.

Em uma API REST, os recursos podem ser disponibilizados através de
endpoints, enquanto métodos HTTP indicam a operação que será realizada.

Por exemplo, uma requisição `POST /users` pode representar uma
solicitação para criação de um novo usuário.

---

## 4. Processamento no Backend

Ao receber a requisição, o backend realiza o processamento necessário.

Entre suas responsabilidades podem estar:

- Validar os dados recebidos;
- Verificar autenticação e autorização;
- Aplicar regras de negócio;
- Consultar ou alterar informações no banco de dados;
- Preparar o resultado da operação.

O servidor permanece disponível para receber novas requisições e
processá-las conforme as regras da aplicação.

---

## 5. Validação e tratamento de erros

Mesmo quando o frontend realiza validações, o backend precisa executar
suas próprias verificações.

A validação no frontend pode oferecer feedback imediato ao usuário,
enquanto a validação no backend ajuda a garantir que os dados recebidos
atendam às regras da aplicação antes de serem processados.

Quando ocorre uma falha, o servidor pode informar o problema ao cliente
por meio de uma resposta HTTP, utilizando códigos de status e mensagens.

---

## 6. A resposta HTTP

Depois do processamento, o servidor prepara uma resposta e a envia
novamente ao cliente.

Uma resposta HTTP pode possuir:

- Código de status;
- Cabeçalhos;
- Corpo da resposta.

Alguns exemplos de códigos de status estudados:

- `200 OK` — requisição realizada com sucesso;
- `401 Unauthorized` — problema relacionado à autenticação;
- `404 Not Found` — recurso não encontrado;
- `500 Internal Server Error` — erro interno no servidor.

Os dados retornados também podem ser representados em JSON.

---

## 7. Atualização do Frontend

Por fim, o frontend recebe a resposta HTTP e interpreta seu conteúdo.

O JavaScript pode utilizar os dados recebidos para atualizar os
elementos da página e apresentar o resultado ao usuário.

Dessa forma, o ciclo pode ser resumido como:

**Usuário → Frontend → HTTP → API → Backend → Processamento →
Resposta HTTP → Frontend → Usuário**

## 📖 Glossário

**Frontend:** Parte da aplicação responsável pela interface e pela
interação direta com o usuário.

**Backend:** Parte da aplicação executada no lado do servidor,
responsável pelo processamento, regras de negócio, validações e acesso
aos dados.

**HTTP:** Protocolo que padroniza a comunicação entre cliente e servidor
através de requisições e respostas.

**API:** Interface que permite que diferentes aplicações ou partes de
um sistema acessem funcionalidades e dados disponibilizados por outra
aplicação.

**REST:** Estilo arquitetural utilizado na construção de serviços em
rede, baseado em princípios como recursos identificados por URIs e
comunicação stateless.

**JSON:** Formato textual utilizado para representar dados, frequentemente
organizados em pares de chave e valor.

**Endpoint:** Endereço disponibilizado por uma API para acessar um
determinado recurso ou funcionalidade.

**Request:** Requisição enviada pelo cliente ao servidor.

**Response:** Resposta enviada pelo servidor ao cliente após o
processamento de uma requisição.

**Stateless:** Princípio em que cada requisição contém as informações
necessárias para ser processada sem depender do contexto de uma
requisição anterior.

## 🔁 Prompts reutilizáveis

Durante o estudo, alguns formatos de prompts se mostraram úteis para
aprofundar o aprendizado e podem ser reutilizados em outros temas:

> Com base exclusivamente nas fontes fornecidas, explique [CONCEITO]
> passo a passo e identifique o papel de cada componente envolvido.

> Compare [CONCEITO A] e [CONCEITO B], destacando suas responsabilidades
> e como eles se relacionam.

> Na resposta anterior, você afirmou que [AFIRMAÇÃO]. Essa afirmação
> é válida em todos os casos? Justifique utilizando apenas as fontes
> fornecidas.

> As fontes fornecidas são suficientes para responder esta pergunta?
> Caso não sejam, identifique quais informações estão ausentes.

> Explique [CONCEITO] utilizando um exemplo prático e depois apresente
> uma definição técnica resumida.
