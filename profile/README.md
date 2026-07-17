<div align="center">

<!-- Header -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a2e1e,50:1B4332,100:2d6a4f&height=220&section=header&text=CMV%20Buffet&fontSize=72&fontColor=ffffff&animation=twinkling&fontAlignY=35&desc=Gest%C3%A3o%20inteligente%20de%20custos%20para%20restaurantes%20e%20buffets&descSize=17&descAlignY=55&descAlign=50" width="100%" />

<!-- Badges -->
<p>
  <img src="https://img.shields.io/badge/CMV-controle_de_custos-1B4332?style=for-the-badge&logo=checkmarx&logoColor=white" />
  <img src="https://img.shields.io/badge/receitas-fichas_técnicas-2d6a4f?style=for-the-badge&logo=bookstack&logoColor=white" />
  <img src="https://img.shields.io/badge/ingredientes-preços_históricos-52b788?style=for-the-badge&logo=databricks&logoColor=white" />
  <img src="https://img.shields.io/badge/multi_tenant-SaaS-95d5b2?style=for-the-badge&logo=building&logoColor=1B4332" />
</p>

<br/>

**CMV Buffet** é uma plataforma SaaS para restaurantes e buffets calcularem e controlarem<br/>
o **Custo de Mercadoria Vendida** — do ingrediente à ficha técnica, em tempo real.

<br/>

<a href="https://app.cmvbuffet.com.br">🌐 Aplicativo</a> &nbsp;·&nbsp;
<a href="https://admin.cmvbuffet.com.br">⚙️ Admin</a>

<br/><br/>

</div>

---

## ⚡ Como funciona

```mermaid
graph LR
  subgraph Restaurante["🍽️ Restaurante"]
    U[Usuário]
  end

  subgraph App["🖥️ cmv-frontend"]
    FE[Next.js App]
  end

  subgraph Admin["⚙️ cmv-admin"]
    ADM[Admin Panel]
    ABFF[Admin BFF]
  end

  subgraph API["🔧 cmv-backend"]
    BE[FastAPI]
    DOM[Domain Layer<br/>Cálculo CMV]
  end

  subgraph DB["🗄️ Supabase"]
    PG[(PostgreSQL<br/>+ RLS)]
  end

  U -->|ficha técnica, ingredientes| FE
  FE --> BE
  BE --> DOM
  DOM -->|CMV, custo por porção| BE
  BE <-->|dados| PG
  ADM --> ABFF
  ABFF <-->|preços globais, ingredientes base| PG

  style Restaurante fill:#f0fdf4,stroke:#1B4332,stroke-width:2px
  style App fill:#dcfce7,stroke:#1B4332,stroke-width:2px
  style Admin fill:#f0fdf4,stroke:#2d6a4f,stroke-width:2px
  style API fill:#d1fae5,stroke:#2d6a4f,stroke-width:2px
  style DB fill:#ecfdf5,stroke:#52b788,stroke-width:2px
```

<br/>

## 🧮 O que resolve

<table>
<tr>
<td width="50%">

### 📊 Cálculo de CMV em tempo real
Fichas técnicas com rendimento, fator de correção e desperdício. O custo por porção é recalculado automaticamente a cada atualização de preço de ingrediente.

### 🧾 Fichas técnicas completas
Cadastre receitas com múltiplos ingredientes, unidades de medida, conversões automáticas e modo de preparo. Gere PDFs prontos para a cozinha.

</td>
<td width="50%">

### 💰 Histórico de preços de ingredientes
Rastreie a variação de preço ao longo do tempo. Saiba exatamente quando seu CMV subiu e por quê — sem surpresas no final do mês.

### 🏢 Multi-estabelecimento
Gerencie vários restaurantes ou unidades com um único login. Dados isolados por estabelecimento, com controle de acesso por papel.

</td>
</tr>
</table>

<br/>

## 🛠 Tech Stack

<div align="center">

### Frontend
<p>
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white" />
</p>

### Backend
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white" />
  <img src="https://img.shields.io/badge/uv-DE5FE9?style=for-the-badge&logo=astral&logoColor=white" />
</p>

### Infraestrutura
<p>
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white" />
  <img src="https://img.shields.io/badge/Cloud_Run-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
</p>

### Dev & CI
<p>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Ruff-FCC21B?style=for-the-badge&logo=ruff&logoColor=black" />
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" />
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white" />
</p>

</div>

<br/>

## 📦 Repositórios

<div align="center">

| Repo | Descrição | Stack |
|:-----|:----------|:------|
| **cmv-frontend** | Aplicativo do restaurante — fichas técnicas, ingredientes, CMV | Next.js · TypeScript · Tailwind |
| **cmv-backend** | API do restaurante — cálculo de CMV, domínio de negócio | Python · FastAPI |
| **cmv-admin** | Painel administrativo — gestão global de ingredientes e preços | Next.js · TypeScript |
| **cmv-admin-backend** | API administrativa — preços base, ingredientes globais | Python · FastAPI |

</div>

<br/>

## 👤 Sobre o criador

<table>
<tr>
<td>

**Daniel Camargo** — Engenheiro full-stack, especialista em automação e gestão de restaurantes.

Construindo o CMV Buffet para que qualquer restaurante possa controlar custos com precisão — sem planilhas.

<p>
  <a href="https://www.linkedin.com/in/daniel13"><img src="https://img.shields.io/badge/LinkedIn-daniel13-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:hello@dans.ch"><img src="https://img.shields.io/badge/Email-hello@dans.ch-EA4335?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

</td>
</tr>
</table>

<br/>

<!-- Footer -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a2e1e,50:1B4332,100:2d6a4f&height=100&section=footer" width="100%" />

</div>
