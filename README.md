# Tales of Legends - Site do Servidor

Este é o código-fonte do site Tales of Legends, um servidor privado de Tales of Pirates.

## Tecnologias Utilizadas

- Next.js 14
- TypeScript
- Tailwind CSS
- SQL Server 2019 (para autenticação e banco de dados do jogo)

## Estrutura do Projeto

- `/src/app` - Páginas do site
- `/src/components` - Componentes reutilizáveis
- `/src/lib` - Utilitários e configurações
- `/public` - Arquivos estáticos

## Configuração para Implantação

### Pré-requisitos

- Node.js 18 ou superior
- Acesso ao SQL Server 2019 com as databases AccountServer e GameDB

### Variáveis de Ambiente

Crie um arquivo `.env.local` na raiz do projeto com as seguintes variáveis:

```
DB_USER=pko_game
DB_PASSWORD=kOM#KB$01tales
DB_SERVER=177.170.70.133
DB_ACCOUNT_DATABASE=AccountServer
DB_GAME_DATABASE=GameDB
```

### Implantação no Vercel

1. Crie uma conta no [Vercel](https://vercel.com) se ainda não tiver
2. Instale a CLI do Vercel: `npm i -g vercel`
3. Execute `vercel login` e siga as instruções
4. Na raiz do projeto, execute `vercel`
5. Configure as variáveis de ambiente no dashboard do Vercel

### Implantação Manual

1. Execute `npm run build` para criar a versão de produção
2. Execute `npm start` para iniciar o servidor

## Funcionalidades

- Sistema de autenticação (registro e login)
- Exibição de rankings de jogadores e guildas
- Informações sobre o servidor e status online
- Páginas de downloads, database e comunidade

## Segurança

Consulte o arquivo [SECURITY.md](./SECURITY.md) para informações sobre as configurações de segurança implementadas.

## Suporte

Para suporte ou dúvidas, entre em contato com o administrador do servidor Tales of Legends.
