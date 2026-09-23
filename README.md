# Portfólio — Larissa Oliveira

Site de portfólio (página única) em HTML puro, pronto para publicar no GitHub e Railway.

## Arquivos

- `index.html` — o site (todo o conteúdo, estilo e a foto já estão dentro desse arquivo).
- `package.json` — diz ao Railway como rodar o site (usa o pacote `serve`).
- `.gitignore` — ignora a pasta `node_modules`.

## 1. Subir no GitHub

1. Crie uma conta em [github.com](https://github.com) (se ainda não tiver).
2. Clique em **New repository**, dê um nome (ex: `portfolio-larissa`) e crie (pode ser público ou privado).
3. Na página do repositório vazio, clique em **uploading an existing file** e arraste os 3 arquivos desta pasta (`index.html`, `package.json`, `.gitignore`).
4. Clique em **Commit changes**.

   *(Se preferir usar o terminal em vez da interface web, veja a seção "Via terminal" no fim deste arquivo.)*

## 2. Publicar no Railway

1. Crie uma conta em [railway.app](https://railway.app) e faça login com o GitHub.
2. Clique em **New Project → Deploy from GitHub repo**.
3. Selecione o repositório `portfolio-larissa` que você acabou de criar.
4. O Railway detecta o `package.json` automaticamente e roda `npm install` + `npm start`.
5. Em **Settings → Networking**, clique em **Generate Domain** para receber um link público (algo como `portfolio-larissa.up.railway.app`).

Pronto — esse link já pode ser usado no currículo, no Instagram (bio) ou enviado para qualquer pessoa.

## Atualizando o site depois

Sempre que quiser mudar algo, edite o `index.html` (ou peça para o Claude editar) e suba a nova versão no GitHub — o Railway republica sozinho a cada novo commit.

## Via terminal (opcional)

```bash
git init
git add .
git commit -m "Primeira versão do portfólio"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/portfolio-larissa.git
git push -u origin main
```
