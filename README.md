<h1 align="center">Olá, eu sou o Matheus 👋</h1>

<p align="center">
  <b>Gestor de performance · Automação com IA · Desenvolvimento de SaaS</b><br/>
  Fundador da <b>FlowPerform</b> — tráfego pago, rastreamento e automação para e-commerce e negócio local.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/matheus-rodrigues-1a74a41a5/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:matheusr2015@gmail.com"><img src="https://img.shields.io/badge/E--mail-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

---

## 🧠 Sobre mim

Trabalho no ponto onde **mídia paga encontra engenharia**. Gerencio Meta Ads e Google Ads para empresas de moda, móveis e decoração, veículos, turismo e games — e, quando a ferramenta certa não existe, eu construo.

- 🎯 Gestão de performance em e-commerce e negócio local (Meta Ads, Google Ads)
- 🔁 Automação *automation-first* com **n8n**, **Claude Code**, **MCP** e **Supabase**
- 📡 Rastreamento server-side: **Meta Conversions API**, deduplicação de eventos e atribuição de vendas no WhatsApp
- 🛠️ Infra própria: **Docker Swarm + Traefik** em VPS Hetzner
- 🇧🇷 Minas Gerais, Brasil

---

## 🚀 O que eu construo

### 📊 SaaS de atribuição de vendas no WhatsApp
> *Problema:* negócios que vendem pelo WhatsApp não sabem qual anúncio gerou a venda — o Meta otimiza no escuro.

Plataforma própria que conecta o inbox do WhatsApp à **Meta Conversions API**: gatilhos na conversa viram eventos de `Purchase` atribuídos à campanha de origem. Hoje é a fonte de verdade de vendas de clientes em produção.

`Next.js 16` `React 19` `TypeScript` `Tailwind 4` `PostgreSQL` `Prisma` `shadcn/ui` `Evolution API` `Meta CAPI` `Docker Swarm` `Traefik`

- Monólito full-stack (App Router, Server Actions, route handlers) com cobrança recorrente de assinaturas
- Deploy em Docker Swarm com TLS automático e migrations no boot
- Auditoria de segurança em fases (auditar → priorizar → corrigir)

---

### 🤖 Agente SDR com IA para agência de turismo
> *Problema:* alto volume de leads de viagens em grupo sem capacidade de qualificação manual.

Agente SDR que atende e qualifica leads no WhatsApp, com **API dedicada + dashboard** de acompanhamento com autenticação, integrado a CRM e ao stack de mensageria.

`Python` `Streamlit` `n8n` `Chatwoot` `Evolution API` `RabbitMQ` `Redis` `PostgreSQL`

---

### 🛍️ Agente de vendas + correção de tracking para e-commerce de moda
> *Problema:* eventos de conversão duplicados/perdidos e atendimento manual sobrecarregado.

- **Agente de vendas com IA** no n8n consultando uma base de produtos no Supabase
- Diagnóstico e correção de bug de rastreio: e-mail *URL-encoded* em cookie quebrava a **deduplicação Pixel ↔ CAPI**
- Assets para anúncios dinâmicos de catálogo (overlays e guia de medidas)

`n8n` `Supabase` `Nuvemshop` `Meta Pixel` `Conversions API`

---

### 🔥 Robô de ofertas para grupo VIP no WhatsApp
Automação no n8n que busca ofertas em **Mercado Livre, Shopee, Amazon e Nuvemshop** e publica automaticamente em um grupo VIP de WhatsApp de uma loja de decoração.

`n8n` `OAuth2` `APIs de marketplaces` `WhatsApp`

---

### 🛋️ Padrão de SEO para catálogo de móveis
Framework editorial de **título SEO, meta description e descrição de produto** para loja de móveis premium na Nuvemshop, com regras anti-canibalização (termo de volume na categoria, long tail no produto) e entrega em HTML pronto para o editor.

`SEO on-page` `Nuvemshop` `Copywriting`

---

### 🧪 Outros projetos

| O que é | Stack |
|---|---|
| Plataforma de sorteios para o nicho de games, com Pixel + CAPI | Web · Meta CAPI · Cloudflare |
| SaaS white-label de streaming com pipeline automático de geração de assets visuais | Node.js · Playwright · TMDB API · PostgreSQL |
| Servidor MCP para operar Google Ads a partir do Claude Code | MCP · Google Ads API |
| Base de conhecimento em Obsidian como memória de longo prazo para agentes de código (lê antes, registra depois) | Obsidian · Claude Code · Codex |

---

## 🏗️ Infraestrutura self-hosted

Toda a operação roda em uma VPS própria orquestrada com Docker Swarm:

```
Traefik (TLS) ─┬─ n8n                (automações)
               ├─ Chatwoot           (atendimento)
               ├─ Evolution API      (WhatsApp)
               ├─ SaaS de atribuição
               ├─ SDR API + Dashboard
               └─ Portainer
Serviços: PostgreSQL · Redis · RabbitMQ
```

---

## 🧰 Stack

**Front & Back**
<p>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white"/>
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white"/>
</p>

**Dados & Infra**
<p>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Traefik-24A1C1?style=flat-square&logo=traefikproxy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Hetzner-D50C2D?style=flat-square&logo=hetzner&logoColor=white"/>
  <img src="https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white"/>
</p>

**Automação & IA**
<p>
  <img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white"/>
  <img src="https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white"/>
  <img src="https://img.shields.io/badge/MCP-111111?style=flat-square"/>
  <img src="https://img.shields.io/badge/WhatsApp_API-25D366?style=flat-square&logo=whatsapp&logoColor=white"/>
</p>

**Mídia & E-commerce**
<p>
  <img src="https://img.shields.io/badge/Meta_Ads-0467DF?style=flat-square&logo=meta&logoColor=white"/>
  <img src="https://img.shields.io/badge/Google_Ads-4285F4?style=flat-square&logo=googleads&logoColor=white"/>
  <img src="https://img.shields.io/badge/Nuvemshop-2C3357?style=flat-square"/>
  <img src="https://img.shields.io/badge/Mercado_Livre-FFE600?style=flat-square&logo=mercadopago&logoColor=black"/>
</p>

---

## 📈 GitHub

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=matheusr2015-sys&show_icons=true&theme=tokyonight&hide_border=true&count_private=true"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=matheusr2015-sys&layout=compact&theme=tokyonight&hide_border=true"/>
</p>

---

<p align="center"><i>Se o dado não chega no Meta, o algoritmo não aprende. Eu faço o dado chegar.</i></p>
