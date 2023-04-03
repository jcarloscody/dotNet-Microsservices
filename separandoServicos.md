## Serviços de dominio
- Domain-driven Design: 
- Um domain service fornece acesso a um único domínio da aplicação e lá suas regras estão contidas.
- começa modelando o domínio. não pensando na persistência.
- avaliar as ações que serão disponibilizdas
- construa o serviço, pensando primeiro no contrato
- REST e RPC(remote procedure call (chamada de ações funcionalidades)) podem andar juntos


## Serviços de Negocios
- a juunçao de varios data service ou serviço de dominio

# Padroes
## Estrangulando o monolito, Strangler pattern
- quebrar o monolito, tirando as funcionalidades dele
- podemos começar isolando os dados
-  ou podemos começar isolando o dominio

## Sidecar Pattern
- determine o processo comum
- construa um modulo compartilhável
- aplique esse sidecar nos serviços que precisam dele
- 