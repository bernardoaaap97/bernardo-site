# Guia de Infraestrutura — Site Pessoal do Bernardo (Atualizado)

Este guia é o "passo a passo de cliques" — coisas que você faz fora do código (GitHub, Vercel, domínio). A construção do site em si é feita pelo Claude Code, lendo o arquivo `02-PROMPT-CLAUDE-CODE-FINAL.md`.

## ✅ Já feito

- [x] Repositório criado no GitHub: `https://github.com/bernardoaaap97/bernardo-site.git`
- [x] Conta no GitHub
- [x] Ambiente VS Code + Claude Code já configurado
- [⏳] Domínio: em processo de compra

## Etapa 1 — Abrir a pasta do projeto no VS Code

1. Crie (se ainda não tiver) uma pasta local chamada `bernardo-site` no seu computador.
2. Abra essa pasta no VS Code: **File → Open Folder...**
3. Abra o terminal integrado: **Terminal → New Terminal** (ou `` Ctrl+` ``).
4. Conecte a pasta local ao repositório remoto que você já criou:
   ```bash
   git init
   git remote add origin https://github.com/bernardoaaap97/bernardo-site.git
   ```
   (Se a pasta já tiver sido clonada direto do GitHub, pule este passo — `git remote -v` mostra se já está conectada.)

## Etapa 2 — Colocar os arquivos do projeto na pasta

Coloque estes arquivos na raiz da pasta `bernardo-site`:
- `02-PROMPT-CLAUDE-CODE-FINAL.md`
- `03-ATIVAR.txt`
- `profile.jpg` (a foto em preto e branco) dentro de uma subpasta `images/` — ou seja, o caminho final deve ser `bernardo-site/images/profile.jpg`

## Etapa 3 — Rodar o Claude Code

1. No terminal do VS Code, inicie o Claude Code (normalmente digitando `claude` ou pelo ícone da extensão, dependendo de como você instalou).
2. Cole o conteúdo do arquivo `03-ATIVAR.txt` no chat do Claude Code.
3. Ele vai ler o `02-PROMPT-CLAUDE-CODE-FINAL.md` e construir o site sozinho: `index.html`, `bio.html`, `about.html`, `style.css`.
4. Confirme que a pasta `images/profile.jpg` existe com a foto antes ou depois dessa etapa — o `<img>` já vai estar referenciando esse caminho.

## Etapa 4 — Subir para o GitHub

No terminal:
```bash
git add .
git commit -m "Initial site build"
git push -u origin main
```
(Se der erro de branch, tente `git push -u origin master` — depende de como o GitHub nomeou a branch padrão.)

## Etapa 5 — Publicar com Vercel

1. Acesse [vercel.com](https://vercel.com) e clique em **Sign Up** → escolha **Continue with GitHub** (assim ele já vê seus repositórios automaticamente).
2. No dashboard, clique em **Add New... → Project**.
3. Selecione o repositório `bernardo-site` na lista e clique em **Import**.
4. Como é um site estático simples (HTML puro), não precisa configurar build command nem output directory — pode deixar em branco/default e clicar em **Deploy**.
5. Em ~1 minuto o Vercel te dá uma URL pública tipo `bernardo-site.vercel.app` — o site já está no ar nesse momento.

## Etapa 6 — Conectar o domínio (quando a compra finalizar)

1. No painel do projeto na Vercel, vá em **Settings → Domains**.
2. Digite o domínio que você comprou e clique em **Add**.
3. A Vercel vai te mostrar os registros DNS exatos que você precisa configurar (geralmente um `A` record ou `CNAME`, dependendo se é o domínio raiz ou um subdomínio como `www`).
4. Vá ao painel do seu registrador de domínio (onde comprou), procure a seção **DNS** ou **Gerenciar DNS**, e adicione exatamente os registros que a Vercel mostrou.
5. Aguarde a propagação (de minutos a até 24h, geralmente bem mais rápido). A Vercel mostra um status "Valid Configuration" quando está tudo certo, e já emite o certificado HTTPS automaticamente.

## Atualizando o site depois

Sempre que quiser mudar algo (texto, adicionar item na Bio, trocar foto):
1. Edite os arquivos localmente (ou peça ao Claude Code para editar).
2. Rode:
   ```bash
   git add .
   git commit -m "Descrição da mudança"
   git push
   ```
3. A Vercel detecta o push automaticamente e republica o site em segundos — não precisa fazer nada manual na Vercel depois da primeira configuração.
