## Como se comunicar
- Api Gateway/BFF(back-end for front-end)(edge service): 
  - Através do API Gateway podemos monitorar acessos a nossa aplicação, podemos ter uma ideia geral de erros que estejam acontecendo, monitorar performance, etc.

## Comunicação Sincrona
- realizamos chamadas e esperamos as respostas.
- **COMO**
  - HTTP: 
    - Padrão RESTFull
    - SOAP
    - GRAPHQ
  - gRPC(Remote Procedure Call, chamada de função remota):
    - mais recente
    - criado pelo google.
    - roda em cima do HTTP2 (então já tem https, transferencia de dados binário e ñ binários... atrelado)
    - chamamos funçoes em outros servidores 
  - Protocolos personalizados
    - abrir um socket de um serviço a outro serviço com TCP

## Comunicacao Assincrona
- CQRS(background tasks, segregação de responsabilidade de comando de ordem e de busca)
- Eventos
  - mensagerias ou plataformas de stream (Kafka, RabitMq)

## FALHAS
- COMUNICAÇÃO SINCRONA
  - circuit breaker: usar um proxy
  - cache: 
- COMUNICACAO ASSINC
  - simples retry
  - retry com back off
  - fila de mensagem morta
  - mensagens devem poder ser lidas fora de ordem
  - mensagens devem poder ser recebidas repetidamente(idempotência)

## Service Discovery
-  Micro podem estar na mesma rede ou em redes separadas, e cada serviço pode estar exposto por um IP.
-  lidar diretamente com o IP pode trazer problemas.
-  DNS:
   -  podemos fazer um na nossa rede.
   -  é um serviço que nos dar nomes de um dominio 