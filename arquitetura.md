### Como funciona a Web
- a internet funciona por meio do protocolo HTTP.
  - um cliente faz um request a um server e o serve envia um response.

- **loadBalance**: servidor que recebe uma requisição e vai mandar estas requisições para servidores diferentes, vai distribuir a carga.

### Aplicação Monolitica
- uma só aplicação que faz tudo. catalogo de serviços, pagamento ...
- Problemas:
  - demora no deploy
  - falhas podem derrubar o sistema todo
  - 1 projeto = 1 tecnologia

### Arquitetura Microsserviços
- cada função será um microsserviço, uma aplicação diferente. e cada serviço terá seu proprio banco de dados
- são uma abordagem arquitetonica e organizacional do desenvolvimento de software na qual o software consiste em pequenos  serviços independentes que se comunicam usando API bem definidas. esses serviços pertencem a pequenas equipes autossuficientes.
-  [Entender quando usar](https://martinfowler.com/bliki/MonolithFirst.html)
- Vantagens:
  - projeto independentes
  - tecnologia independentes
  - falha em 1 serviço é isolada
  - deploy menores e mais rápidos
- Desvantagens
  - maior complexidade de desenvolvimento e infra
  - debug mais complexo: pq nela temos uma stack trace, como um serviço chama outro, para rastrear o problema fica dificio
  - comunicacao entre serviços deve ser bem pensada
  - diversas tecnologias pode ser um problema
  - monitoramento é crucial e mais complexo
****

## Tipos de Micro
- Data Servie
  - simplesmente vai expor dados, como se fosse uma fina camada antes do bd. vai manter os dados consistentes
- Business Service
  - fornece operaçoes mais complexas, 
- Translation Service
  - acessa recursos externos mas mantendo um certo controle.
- Edge Service
  - serviço de ponta. entrega diretamente para o cliente. pode ter necessidades espeficicas.