# UUID Generator

PWA de página única para geração de UUIDs v4 seguros. Funciona offline, instalável no iPhone, Android e Desktop.

## Como rodar localmente

```bash
python3 -m http.server 8000
# abra http://localhost:8000
```

## Como buildar / deploy

Não há etapa de build — são arquivos estáticos puros. Para publicar no GitHub Pages:

1. Vá em **Settings → Pages** do repositório
2. Source: `main` / `/ (root)`
3. Salve — o site estará em `https://<user>.github.io/uuid_website/`

## Testar como PWA

**Desktop (Chrome/Edge):** ícone de instalação aparece na barra de endereço ao abrir o site.

**Android:** banner "Adicionar à tela inicial" aparece automaticamente.

**iPhone (Safari):** Compartilhar → Adicionar à Tela de Início.

**Offline:** depois de instalado, abre e funciona completamente sem conexão.

## Stack

- HTML + CSS + JS puros (zero dependências, zero build)
- `crypto.randomUUID()` com fallback via Web Crypto API
- PWA: `manifest.json` + Service Worker (cache-first, offline total)
- Design: glassmorphism dark, Apple HIG
