# Excom Turismo — site novo

Redesign estático (HTML/CSS/JS puros, sem framework e sem etapa de build).

## Antes de publicar

1. Abra `images/MANIFEST.md` e baixe as 11 imagens listadas para dentro da
   pasta `images/`, com os nomes exatos indicados. Sem isso, os espaços das
   fotos ficam em branco.

## Subir para o GitHub

```bash
cd excom-turismo-site
git init
git add .
git commit -m "Site novo da Excom Turismo"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
git push -u origin main
```

## Deploy no Render

**Opção A — pelo painel (mais simples):**
1. No Render, clique em **New > Static Site**.
2. Conecte o repositório do GitHub que você acabou de criar.
3. Em **Build Command**, deixe em branco (ou `echo "sem build"`).
4. Em **Publish Directory**, coloque `.` (a raiz do repositório).
5. Clique em **Create Static Site**.

**Opção B — pelo Blueprint (`render.yaml`):**
O arquivo `render.yaml` já vai junto no repositório. No Render, clique em
**New > Blueprint**, conecte o repositório e clique em **Apply** — ele lê o
`render.yaml` sozinho e cria o serviço com as configurações corretas.

## Estrutura

```
excom-turismo-site/
├── index.html          → a página inteira
├── images/              → fotos referenciadas pelo index.html
│   └── MANIFEST.md      → lista do que baixar e onde salvar
├── render.yaml           → configuração de deploy (Blueprint do Render)
└── README.md             → este arquivo
```

## Domínio próprio

Depois do primeiro deploy, em **Settings > Custom Domains** no Render dá para
apontar `www.excomturismo.com.br` (ou o domínio que preferir) para o site
novo.
