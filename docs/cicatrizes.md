# "Cicatrizes" do Processo de Aprendizagem

Durante a exploração das fontes com o NotebookLM, algumas respostas
levantaram mais dúvidas.

Esses pontos foram registrados como "cicatrizes" do processo, pois
contribuíram para o refinamento dos prompts e para a construção do
conhecimento ao longo do projeto.

---

## Cicatriz 01 — O JSON parecia obrigatório

### O que aconteceu

Na primeira explicação sobre o fluxo entre frontend e backend, o JSON
apareceu em diversas etapas da comunicação.

A forma como a resposta foi apresentada poderia levar à interpretação
de que toda requisição HTTP utiliza JSON.

### Como investiguei

Foi realizado um novo prompt questionando diretamente essa interpretação:

> Toda requisição HTTP entre frontend e backend utiliza JSON?

### O que descobri

Não. O HTTP não depende do JSON para funcionar.

O HTTP é o protocolo utilizado para a comunicação, enquanto o JSON é
um formato de representação de dados que pode ser transportado no corpo
de uma mensagem HTTP.

Essa investigação também ajudou a diferenciar três conceitos que
inicialmente apareciam muito próximos: HTTP, REST e JSON.

---

## Cicatriz 02 — As fontes também possuem limites

### O que aconteceu

Durante o estudo surgiu uma dúvida relacionando a comunicação entre
frontend e backend com um conteúdo estudado anteriormente: o modelo OSI.

### Limitação encontrada

Ao questionar o NotebookLM, foi identificado que as fontes selecionadas
abordavam HTTP, TCP, UDP, sockets e a pilha TCP/IP, mas não apresentavam
material suficiente sobre as sete camadas formais do modelo OSI.

Por isso, não era possível construir uma comparação completa utilizando
exclusivamente as fontes fornecidas.

### O que aprendi

A qualidade de uma resposta baseada em fontes também depende da
curadoria realizada antes da interação com a IA.

Identificar que uma fonte não é suficiente para responder determinada
pergunta é tão importante quanto encontrar uma resposta.

---

## Cicatriz 03 — "O backend valida" não era suficiente

### O que aconteceu

Na explicação inicial, foi informado que o backend recebe e valida uma
requisição antes de executar a lógica necessária.

Porém, essa explicação gerou uma nova dúvida:

> Como essa validação realmente acontece e como um erro retorna ao
> frontend?

### Como investiguei

Foram realizados novos questionamentos sobre validação dos dados,
tratamento de erros e sobre a necessidade de validar informações
novamente no backend quando o frontend já realizou uma validação.

### O que aprendi

A validação realizada no frontend e a realizada no backend possuem
responsabilidades diferentes.

O frontend pode verificar informações e fornecer feedback imediato ao
usuário, enquanto o backend precisa aplicar suas próprias validações
antes de executar determinadas operações.

Também compreendi melhor como respostas HTTP e códigos de status podem
ser utilizados para comunicar erros novamente ao cliente.

---

# Conclusão

As principais dificuldades não foram por respostas erradas da IA. 

Elas apareceram principalmente como simplificações, novas dúvidas e
limitações das próprias fontes.

O processo de questionar as respostas iniciais foi fundamental para
transformar uma explicação geral sobre frontend e backend em um estudo
mais aprofundado sobre HTTP, REST, JSON, validação e comunicação
cliente-servidor.
