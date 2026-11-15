# União da Diversão — site da comunidade

Site estático responsivo inspirado no vídeo enviado: identidade branca e azul, navegação superior, cartões, seções de servidor, regras, equipe, utilidades, denúncia, formulários e área reservada.

## Estrutura

```text
uniao-da-diversao-site/
├── index.html
├── README.md
└── assets/
    ├── css/styles.css
    ├── js/app.js
    ├── js/config.js
    └── img/
        ├── logo.svg
        └── favicon.svg
```

## Como executar

Abra `index.html` no navegador ou publique a pasta em GitHub Pages, Netlify ou outro serviço de hospedagem estática.

## Personalização

Edite `assets/js/config.js` para atualizar nome, convite e e-mail público. Para alterar equipe e conteúdo, edite `index.html`.

## Importante: funcionalidades que exigem backend

Este pacote é a interface frontend. Formulários são validados no navegador e podem abrir o aplicativo de e-mail se `contactEmail` estiver preenchido. Para receber denúncias/inscrições automaticamente, salve os dados em um backend com validação e proteção contra spam.

A área de moderadores **não é um painel protegido nesta versão**. O login real deve usar Discord OAuth2 no servidor (Authorization Code flow), validar a identidade e conferir os cargos/permissões no servidor Discord. Nunca coloque bot token, client secret, senhas ou credenciais em arquivos públicos do frontend.

Para ativar OAuth2:
1. Crie uma aplicação no Discord Developer Portal.
2. Configure a Redirect URL HTTPS.
3. Implemente a troca do `code` no backend, mantendo o client secret somente no servidor.
4. Consulte a API do Discord e valide os cargos/permissões antes de liberar rotas administrativas.
5. Troque o link de exemplo no botão da área de moderadores por uma rota do seu backend.

## Link do servidor

https://discord.gg/SSp8fqcwg9

## Próxima etapa

Conectar o projeto a um repositório GitHub existente e implementar backend/OAuth2. O repositório de destino ainda precisa ser confirmado.
