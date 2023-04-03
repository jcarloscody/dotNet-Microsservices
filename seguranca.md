## Segurança Geral
- Segurança de transporte
  - HTTPs
- Segurança no repouso 
  - Criptografia
  - Anonimização

## Autenticação e Autorização
- autenticação: garante que o cliente é o cliente
  - Basic HTTP
    - autorização basica no http
    - em todas as requisições irá ser colocado a senha e o usuário no cabeçalho. 
  - Token (JWT)
    - após o login, o server envia um token
    - a cada requisição o cliente envia o token
  - OAuth
    - usa serviço de terceiro
    - delega a responsabilidade para tratar a auth
  - OpenID Connect
    - parece com a ideia o OAuth
- Autorização: se a pessoa autenticada pode realizar tal ação
  - ACL (Access control list)
    - lista de controle de acesso
  - RBAC(Role-based access control)
    - controle de acesso baseado em papeis
  - On Behalf of
- https://www.youtube.com/watch?time_continue=1&v=B-7e-ZpIWAs&embeds_euri=https%3A%2F%2Fcursos.alura.com.br%2F&source_ve_path=MjM4NTE&feature=emb_title&ab_channel=DiasdeDev
- https://www.youtube.com/watch?v=MZetkcs2xIo&t=12s&ab_channel=DiasdeDev



## Defense in Depth
- todo sistema está propenso a ataques


## Ambiente de Execução
- Desenvolvimento
- Staging/QA
  - testes de performance
  - smoke tests
- Homologacao
  - Alguém de negócio vai usar para garantir que está tudo certo
- Produção
  - cliente final