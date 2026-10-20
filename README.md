# Bruno Ghiggi — Encontre suas fotos

Página de links para fotos de eventos esportivos e treinos, pronta para o GitHub Pages.

## Estrutura
- `index.html` — página principal
- `fotto/` — redirecionamento rastreável para a Fotto
- `foco/` — redirecionamento rastreável para a Foco Radical
- `whatsapp/` — redirecionamento rastreável para o WhatsApp
- `instagram/` — redirecionamento rastreável para o Instagram (@brunoghiggi)
- `404.html` — página de erro amigável
- `bruno.jpg` — foto do cabeçalho
- `img/` — logos da Fotto e da Foco Radical (versão clara e escura)

## Publicar
1. Envie o **conteúdo** desta pasta para a raiz do repositório (o `index.html` precisa ficar na raiz, não dentro de uma subpasta).
2. Settings → Pages → *Deploy from a branch* → `main` → `/ (root)` → Save.
3. Aguarde 1–2 minutos e acesse `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

Os links são relativos, então funcionam tanto em repositório de projeto quanto em `SEU-USUARIO.github.io`.

## Links rastreáveis para divulgar
- `.../fotto/` · `.../foco/` · `.../whatsapp/` · `.../instagram/`

## Google Analytics 4 (opcional)
Troque `G-XXXXXXXXXX` pelo seu ID nos quatro arquivos `fotto/index.html`, `foco/index.html`, `whatsapp/index.html` e `instagram/index.html`.
Cada acesso gera o evento `redirect_click` com os parâmetros `plataforma` e `destino`.

## Últimos eventos e treinos (sem precisar refazer upload)
A lista vem de uma planilha Google. Editou a planilha, o site mostra na próxima abertura (o Google pode levar até ~5 min para atualizar o CSV publicado).

1. Crie uma planilha no Google Sheets com estas colunas na linha 1:
   `Data | Evento | Tipo | Plataforma | Link`
   - **Data**: dd/mm/aaaa
   - **Tipo**: Evento ou Treino (treino aparece com etiqueta verde)
   - **Plataforma**: Fotto ou Foco Radical
   - **Link** (opcional): link direto da galeria; se vazio, usa a página da plataforma
2. Arquivo → Compartilhar → **Publicar na Web** → escolha a aba → formato **CSV** → Publicar → copie o link.
3. No `index.html`, cole o link em `const PLANILHA_CSV='';` (só uma vez).

O site mostra os 6 mais recentes (`MAX_EVENTOS`). Se a planilha estiver vazia ou fora do ar, a seção some sem quebrar a página.
