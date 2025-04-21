# Configurações de Segurança para o Tales of Legends

Este arquivo contém informações importantes sobre as configurações de segurança implementadas no projeto Tales of Legends.

## Proteção de Credenciais

As credenciais do banco de dados estão armazenadas em variáveis de ambiente para maior segurança. Para configurar as variáveis de ambiente no Vercel ou em outra plataforma de hospedagem, adicione as seguintes variáveis:

```
DB_USER=pko_game
DB_PASSWORD=kOM#KB$01tales
DB_SERVER=177.170.70.133
DB_ACCOUNT_DATABASE=AccountServer
DB_GAME_DATABASE=GameDB
```

## Middleware de Autenticação

O middleware de autenticação protege rotas que requerem login. As rotas protegidas incluem:
- /dashboard
- /profile

Usuários não autenticados serão redirecionados para a página de login.

## Proteção contra CSRF

Implementamos proteção contra Cross-Site Request Forgery (CSRF) para todas as requisições POST.

## Hashing de Senhas

As senhas são armazenadas no banco de dados usando hash MD5, conforme o esquema original do servidor Tales of Pirates.

## Cookies Seguros

Os cookies de sessão são configurados com as seguintes propriedades de segurança:
- httpOnly: true (não acessível via JavaScript)
- secure: true em produção (enviado apenas via HTTPS)
- maxAge: 7 dias

## Recomendações Adicionais

1. Configure HTTPS no seu domínio para garantir comunicação segura
2. Considere implementar autenticação de dois fatores no futuro
3. Realize backups regulares do banco de dados
4. Mantenha as dependências do projeto atualizadas
