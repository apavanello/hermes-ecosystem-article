# Hermes Agent Ecosystem — Artigo (pt-BR)

Artigo em HTML standalone sobre a topologia do ecossistema Hermes Agent — três nós (OPi 3b, PC pessoal, OCI), fluxo principal, memória em duas camadas, external systems e observabilidade.

Publicação alvo: **Medium** + LinkedIn. O Medium não aceita upload de HTML, mas importa direto de uma URL pública — GitHub Pages serve essa função. O LinkedIn posta um resumo + link para cá.

## Estrutura

```
.
├── index.html              # artigo completo (pt-BR, ~1500 palavras)
├── README.md
├── .nojekyll               # GH Pages: pula build do Jekyll
└── assets/
    └── diagrams/           # 5 PNGs exportados via mermaid-cli
        ├── 01-request-flow.png
        ├── 02-memory-knowledge.png
        ├── 03-external-systems.png
        ├── 04-observability.png
        └── 05-ecosystem-main.png
```

## Como publicar no GitHub Pages

1. Crie um repo novo no GitHub (ex: `hermes-ecosystem-article`), público.

2. Suba a pasta inteira (`hermes-ecosystem-article/`) como raiz do repo:

```bash
cd /home/apavanello/diagrams/hermes-ecosystem-article
git init
git add .
git commit -m "feat: artigo pt-BR sobre ecossistema Hermes"
git branch -M main
git remote add origin git@github.com:SEU_USER/hermes-ecosystem-article.git
git push -u origin main
```

3. No GitHub: `Settings → Pages → Source: Deploy from a branch → Branch: main → Folder: / (root) → Save`.

4. Espere ~1 min. Seu artigo estará em:

```
https://SEU_USER.github.io/hermes-ecosystem-article/
```

5. Importar no Medium:

   - Abra o artigo no navegador em `https://SEU_USER.github.io/hermes-ecosystem-article/`
   - Use a extensão **"Save to Medium"** (Chrome) ou **"Medium Import"** para importar a URL
   - O Medium cria um draft com formatação preservada (parágrafos, headings, imagens)

## Como publicar no LinkedIn

Texto curto (~300 palavras), com:

- Abertura com o hook de fragmentação (3 pontos)
- Imagem destaque: `assets/diagrams/05-ecosystem-main.png` + legenda
- Resumo do fluxo principal em 1 parágrafo
- Link `https://SEU_USER.github.io/hermes-ecosystem-article/` no fim

LinkedIn não renderiza HTML, mas permite link preview com imagem + título via Open Graph — que essa página não tem ainda (opcional, pode pular).

## Customizar

- **Cores / fontes:** editar `:root` no `<style>` do `index.html`
- **Tempo de leitura / kicker:** editar `header.title` no `index.html`
- **Substituir diagramas:** sobrescrever PNGs em `assets/diagrams/`. Fonte original em `/home/apavanello/diagrams/*.mmd`

## Próxima parte

`Parte 2 — montagem do zero`: comandos, arquivos de configuração, armadilhas.
