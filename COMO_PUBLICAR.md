# KIXI AI — Como publicar (Netlify, grátis)

**Estrutura atual: site multi-página a sério.** Cada braço da KIXI tem o
seu próprio URL — não é mais tudo âncoras numa única página:

```
/                                          → homepage (resumo)
/infrastructure/                          → arquitetura de 6 camadas
/solutions/                               → agentes de IA (órbita)
/consulting/                              → indústrias
/insights/                                → galeria de Executive Briefs
/insights/primeiro-colaborador-digital/   → o artigo
/about/                                   → Sobre
/contact/                                 → Contacto (com email real)
```

## Passo 0 — Cria uma conta Google dedicada à KIXI (antes de tudo)

Não uses a tua conta pessoal, nem precisas de esperar pelo domínio.
Cria já um Gmail só para a empresa — ex: `kixiai@gmail.com` (se estiver
livre) ou uma variação próxima. É normal e temporário: a maioria das
empresas começa assim. Usa **esta** conta para tudo o que vem a seguir
(Search Console, Netlify, redes sociais da KIXI).

Quando um dia tiveres email profissional no domínio (ex: via Google
Workspace ou Zoho Mail), nada se perde — a conta Gmail continua a existir
como "login de backend", só deixas de a dar às pessoas como contacto.
Podes até reencaminhar o Gmail antigo para o email novo.

**Nota técnica:** ter o domínio sozinho não dá emails automaticamente —
precisa de um serviço de email configurado por cima (Google Workspace,
Zoho Mail, etc.), como já vimos antes.

## Passo a passo (5 minutos, sem cartão de crédito)

1. Vai a **app.netlify.com/drop**
2. Arrasta esta pasta inteira (`kixi_deploy`) para o browser
3. Em segundos, a Netlify dá-te um link tipo:
   `https://effulgent-souffle-a1b2c3.netlify.app`
   → **já está no ar e já dá para partilhar.**
4. Cria uma conta grátis (email ou GitHub) para não perderes este site
   passado uns dias — sem conta, o link é temporário.
5. Depois de teres conta: **Site settings → Change site name** →
   escolhe algo como `kixi-ai` → o teu link passa a
   `https://kixi-ai.netlify.app` (mais fácil de partilhar já).

## Quando comprares o domínio kixi.ai

**Site settings → Domain management → Add a domain** → escreve `kixi.ai` →
a Netlify diz-te exatamente que 2 registos DNS adicionar no sítio onde
compraste o domínio. Depois disso, o HTTPS fica automático.

## Uma coisa a lembrar depois de publicares

As tags de partilha (Open Graph) e o mapa do site (`canonical`, JSON-LD)
neste momento apontam para `https://kixi.ai/...` como placeholder. Antes de
teres o domínio, troca isso pelo teu link temporário da Netlify
(`https://kixi-ai.netlify.app/...`) nos dois ficheiros:

- `index.html`
- `insights/primeiro-colaborador-digital/index.html`

Procura por `https://kixi.ai` (usa Ctrl+F) e substitui pelo teu link atual.
Quando comprares o domínio a sério, repete a substituição uma última vez.

## Testar se a partilha ficou bem

Depois de publicado, cola o teu link em **opengraph.xyz** — mostra-te
exatamente como vai aparecer no WhatsApp/LinkedIn antes de partilhares
a sério.

## Como aparecer no Google a pesquisar "KIXIAI"

Publicar o site **não avisa o Google sozinho**. Sem este passo, pode
levar semanas a ser descoberto por acaso. Com este passo, normalmente
leva dias.

1. Vai a **search.google.com/search-console** e entra com uma conta Google.
2. Escolhe **"Prefixo do URL"** e cola o teu link da Netlify
   (ex: `https://kixi-ai.netlify.app`).
3. A Google pede para confirmares que o site é teu — a forma mais simples
   é escolher **"ficheiro HTML"**: ela dá-te um ficheiro para descarregares
   e colocares dentro desta mesma pasta antes de voltares a publicar
   (arrastas a pasta outra vez para a Netlify, com esse ficheiro lá dentro).
4. Depois de verificado: **Sitemaps** (menu lateral) → cola `sitemap.xml`
   → Enviar. Isto já está incluído nesta pasta.
5. Por fim, em **Inspeção de URL**, cola o link da tua página inicial e
   carrega em **"Pedir indexação"**. Este é o botão que diz ao Google
   "vem cá ver isto agora", em vez de esperar que apareça sozinho.

Depois disto, pesquisar "KIXIAI" no Google costuma mostrar resultado em
alguns dias — é um termo único, sem concorrência, por isso quando o
Google o indexar, tende a aparecer em 1º lugar.

**Nota:** quando comprares o domínio `kixi.ai`, repete este processo de
verificação no Search Console para o domínio novo — a verificação não
transita automaticamente do subdomínio da Netlify.
