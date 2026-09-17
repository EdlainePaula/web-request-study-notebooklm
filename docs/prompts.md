# 🤖 Engenharia de Prompts

Durante o projeto, o NotebookLM foi utilizado como ferramenta de
aprendizagem a partir das fontes selecionadas.

Os prompts foram construídos de forma progressiva. A partir das respostas
obtidas, novas dúvidas foram levantadas.

---

## Prompt 01 — Mapeamento do fluxo Frontend → Backend

### Objetivo

Compreender inicialmente todo o caminho percorrido durante a comunicação
entre frontend e backend.

### Prompt 1

> Com base exclusivamente nas fontes fornecidas, explique passo a passo
> o que acontece desde o momento em que um usuário realiza uma ação em
> uma interface web até o recebimento da resposta pelo frontend.
> Identifique em cada etapa o papel do cliente, servidor, protocolo HTTP,
> API REST e JSON. Cite as fontes utilizadas para sustentar cada parte
> da explicação.

### Resultado

A resposta dividiu o processo em cinco etapas:

1. Ação do usuário e preparação no frontend;
2. Disparo da requisição HTTP;
3. Recebimento e processamento no backend;
4. Construção da resposta HTTP;
5. Processamento e renderização da resposta no frontend.

A partir dessa resposta surgiram novas dúvidas, principalmente sobre
o papel do JSON, os protocolos envolvidos na comunicação e a validação
dos dados.

---

## Prompt 02 — JSON é obrigatório?

### Objetivo

Verificar uma possível generalização identificada na primeira resposta
e diferenciar HTTP, REST e JSON.

### Prompt

> Na resposta anterior, descreveu JSON como parte do envio de dados
> entre frontend e backend. Com base exclusivamente nas fontes fornecidas,
> esclareça: toda requisição HTTP entre frontend e backend utiliza JSON?
> Explique a diferença entre HTTP, API REST e JSON e mostre qual é a
> responsabilidade de cada um durante a comunicação. Caso alguma das
> fontes não seja suficiente para sustentar determinada afirmação,
> indique essa limitação.

### Aprendizado

Foi identificado que JSON não é obrigatório em toda comunicação HTTP.
HTTP é o protocolo responsável pela comunicação, REST é um estilo
arquitetural e JSON é um formato utilizado para representar e
transportar dados.

---

## Prompt 03 — Relação com o modelo OSI

### Objetivo

Relacionar os novos conhecimentos sobre comunicação web aos conceitos
de redes de computadores.

### Prompt

> Os protocolos de comunicação que acontecem nessa etapa do frontend
> ao backend são o mesmo que as camadas de comunicação do modelo OSI,
> por exemplo?

### Resultado

A resposta conseguiu relacionar HTTP à camada de aplicação e abordar
TCP, UDP, sockets e a pilha TCP/IP.

Entretanto, foi identificado que as fontes selecionadas não abordavam
formalmente as sete camadas do modelo OSI e, portanto, não permitiam
uma comparação completa utilizando exclusivamente o material fornecido.

---

## Prompt 04 — Validação e tratamento de erros

### Objetivo

Entender o que acontece com os dados depois que uma requisição chega
ao backend.

### Prompt

> Quando uma API recebe dados enviados pelo frontend, como o backend
> verifica se esses dados são válidos? Em que momento ocorre a validação
> e como os erros são tratados e informados novamente ao frontend?

### Aprendizado

A investigação mostrou que o backend realiza validações antes de
efetivar determinadas operações e pode comunicar falhas ao cliente
por meio das respostas HTTP, utilizando códigos de status e mensagens
no corpo da resposta.

---

## Prompt 05 — Frontend x Backend na validação

### Objetivo

Entender por que a validação no backend continua necessária quando
o frontend já realizou verificações.

### Prompt

> Se o frontend já pode validar os dados antes de enviá-los, por que
> o backend precisa validar os mesmos dados novamente?

### Aprendizado

A validação no frontend contribui para uma experiência mais rápida
para o usuário, enquanto o backend precisa aplicar suas próprias
validações para proteger regras de negócio e a integridade dos dados.

Também foi observado que uma API pode receber requisições de diferentes
clientes, e não exclusivamente da interface frontend desenvolvida para
a aplicação.

---

## Prompt 06 — Stateless e autenticação

### Objetivo

Investigar uma aparente contradição encontrada durante o estudo sobre
APIs REST.

### Prompt

> Você afirmou que o backend verifica autenticação e autorização.
> Se uma API REST é stateless e não mantém o estado do cliente entre
> requisições, como um usuário consegue permanecer autenticado?

### Aprendizado

O conceito de stateless não significa ausência de autenticação.
Cada requisição precisa fornecer as informações necessárias para que
o servidor consiga processá-la e verificar a identidade e as permissões
do cliente.

Essa investigação ajudou a diferenciar o estado da comunicação REST
do processo de autenticação de um usuário.
