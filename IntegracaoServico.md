## Ponto único de entrada - API Gateway (Padrao)
- problema: clientes acessando livremente os serviços geram caos.
- gateway fornece um proxy, uma fachada, para as necessidades reais.
- Desvantagem: esse portão de entrada pode se tornar um ponto central de falha
- Comportamento
  - simplesmente autorizar e redirecionar os requests
  - uso de decorator para adicionar informaçoes necessárias aos requests (Headrs)
  - limitar o acesso ou conteudo trafegado


## Agregar processos (process aggregator pattern)
- serviços de negocio agregam servicos de dominio
- process aggregator agregam servicos de negocio
- agregadores fazem as chamadas para os serviços necessários e montam a resposta correta
- pode (e deve) ter lógica de processamento
- Construção
  - definir um novo modelo para representar os dados agregados


## Gateways espeficicos - Edge pattern
- para determinado client
- Quando clientes diferentes possuem necessidades diferentes
- foco nas necessidades reais de determinados clientes
- Constuindo
  - identificar os clinete e necessidades
  - contratos especificos
  - modificacao dos dados que sao transferidos para garantir a otimização do processo
  - existe  a possibilidade de ter apenas Edges,  e não gateways

## Single service database
- problema: escalabilidade do serviço e do banco  sao fortemente relacionados
- solução: cada serviço terá o seu proprio
- a! Com cada serviço tendo seu próprio banco, a escalabilidade do serviço e banco pode ser feita em conjunto. Assim, serviços que recebem poucos acessos podem ter bancos menos potentes e mais baratos, e vice-versa.

## shared service database
- problema: as vezes precisamos centralizar os dados
- solucao: trata o unico banco como se fosse separado

## Padroes de codificacao (CQRS - COMMAND QUERY RESPONSIBILITY SEGREGATION, segregacao da responsabildade entre o comando e uma busca)
- no seu nucleo é a noção que podemos usar modelos diferentes para buscar uma informação e para atualizar/inserir informaçao. modelos diferentes para escrever e ler. em algumas situaçoes estas separações podem ser muito valiosas, em uma situação pode ser de escrita e outro de leitura, porem em muito sistemas ele adiciona uma complexidade muito arriscada
- https://www.youtube.com/watch?v=yd6V4w19iJU&ab_channel=EximiaCo-Excel%C3%AAnciaTecnol%C3%B3gica


## Eventos Assíncronos - Asynchronous eventing (padroes)
- determinados problemas não podem ser resolvidos na hora (em tempo real)
- um serviço emite um evento que será tratado em seu devido tempo
- tecnologias como mensagerias e serviços de stream de dados brilham. 

## Agregação de Logs
- Formato de log DEVEM ser compartilhado entre serviços 
- Uma taxonomia comum deve ser compartilhada
- logs de monolitos são agregados por padrao . 
- parte da tarefa de agregação pode ser o parsing dos logs para caracterizar corretamente
- **Rastrenado chamadas**
  - uma parte importante de realizar logs é rastrear as chamadas de uma execução
  - devemos poder reconstruir uma operação a partir de um identificador
  -  isso  é o equivalente a call stack de um sistema monolittico
  -  use padrao de trace id para gerar logs
  -  use ferramenta de gerenciamento (apms) para visualizar
  -   Logs estão para a saúde do sistema assim como exames estão para nossa saúde física. Através de logs podemos identificar informações muito valiosas sobre nossa aplicação.
  -   Os logs são o que nos permitem montar uma espécie de call stack ou stack trace, ou seja, através de logs conseguimos reproduzir uma execução e depurá-la.

## Agregando Métricas
- Enquanto logs precisam de desenvolvimento, métricas só precisam de instrumentação
- métricas nos permitem saber o que está acontecendo em determinado momento
- construa ou use dashboards de alto nível para ter uma fácil visão do status atual da aplicação
- depois tenha dashboards especificos para cada serviço com mais detalhes