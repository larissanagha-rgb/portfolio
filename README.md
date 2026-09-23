# Portfólio — Larissa Oliveira

Site de portfólio (página única) em HTML puro, publicado no Railway usando um contêiner Nginx simples — sem depender de Node/npm, então evita os erros de build.

## Arquivos

- `index.html` — o site (conteúdo, estilo e foto já estão dentro desse arquivo).
- `Dockerfile` — diz ao Railway para rodar um servidor Nginx com esse HTML dentro.
- `default.conf.template` — configuração do Nginx (ajusta a porta automaticamente).

**Importante:** se você já tinha subido `package.json` ou `.gitignore` de uma tentativa anterior, apague-os do repositório — não são mais necessários com essa versão.

## 1. Subir no GitHub

1. Acesse o repositório que você já criou (ou crie um novo em [github.com/new](https://github.com/new)).
2. Clique em **Add file → Upload files**.
3. Arraste os 3 arquivos desta pasta: `index.html`, `Dockerfile`, `default.conf.template`.
4. Se existirem `package.json` ou `.gitignore` de antes, delete-os pela interface do GitHub (abra o arquivo → ícone da lixeira).
5. Clique em **Commit changes**.

## 2. Publicar no Railway

1. No [railway.app](https://railway.app), abra o projeto que você já criou (ou crie um novo com **New Project → Deploy from GitHub repo**).
2. Selecione o repositório do portfólio.
3. O Railway vai detectar o `Dockerfile` automaticamente e usar ele para o build (não precisa configurar nada).
4. Espere o deploy terminar (aba **Deployments**, status **Success**).
5. Vá em **Settings → Networking → Generate Domain** para gerar o link público.

Se o deploy anterior (com `package.json`) ainda estiver configurado como "Nixpacks" nas Settings do serviço, vá em **Settings → Build** e confirme que o Builder está como **Dockerfile** — o Railway normalmente troca sozinho ao detectar o arquivo.

## Atualizando o site depois

Edite o `index.html` (ou peça para o Claude editar), suba a nova versão no GitHub, e o Railway republica automaticamente a cada commit.
