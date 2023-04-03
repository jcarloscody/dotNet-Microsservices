## Composição de micro
- é uma aplicação que tem acesso a determinado dados, um serviço pequeno que se comunica com outros. 
- cada micro é o dono e gerenciador de seus proprios dados.
-  Uma máquina (servidor) pode ser considerada um componente. Várias aplicações em uma mesma máquina podem ser vários componentes. Um serviço de apoio (como banco de dados ou fila de mensageria) pode ser um componente. Qualquer coisa que efetivamente componha o serviço, é um componente.

## Contratos entre Micro
- um micro expoe alguma forma de comunicação (uma api). isso é o contrato entre este micro e seus clientes.
- MODIFICAÇÕES
  - faça apenas modificacoes aditivas
    - novos endpoints
  - versionamento de APIs
    - ao lançar uma v2, a v1 deve continuar funcionando


## Identificando as Barreiras
- DDD - Bounded Context. como separa a aplicação em modulos, e como estes modulos podem virar serviços futuramente.