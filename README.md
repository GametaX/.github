# GametaX

**Software sob medida, da arquitetura à entrega.**

Fábrica de software e consultoria de engenharia especializada em **C# / .NET** e **React**.

---

A **GametaX** projeta e constrói software sob medida para empresas que precisam de
sistemas confiáveis, escaláveis e moldados ao seu negócio. Atuamos de ponta a
ponta — da definição da arquitetura à entrega em produção — com foco em
engenharia sólida e parceria de longo prazo.

## O que fazemos

- **Sistemas web sob medida** — plataformas de gestão, back-offices e produtos
  internos construídos para o problema real do cliente, sem caixas-pretas.
- **APIs e integrações** — APIs robustas e integrações com terceiros (pagamentos,
  ERPs, fiscal, logística) para conectar e automatizar operações.
- **Consultoria técnica e arquitetura** — apoio em decisões de arquitetura,
  padronização, code review e estruturação de squads.

## Por que a GametaX

- **Engenharia sólida em C#/.NET e React** — backend robusto em ASP.NET Core com
  interfaces modernas em React (SSR). Confiabilidade e performance no centro de tudo.
- **Arquitetura escalável e padronizada** — um padrão consistente entre os
  produtos, com backend em Vertical Slice Architecture e separação clara entre
  interface, API e processamento assíncrono, pronto para crescer.
- **Parceria de longo prazo** — acompanhamos a evolução do produto além da
  entrega inicial, com proximidade e continuidade.

## Stack

| Camada           | Tecnologias                                                   |
| ---------------- | ------------------------------------------------------------- |
| Backend          | C# · .NET · ASP.NET Core                                       |
| Arquitetura      | Vertical Slice Architecture (VSA) · CQRS                      |
| Frontend         | React (SSR) · TypeScript · Vite · Next.js                     |
| Dados            | PostgreSQL · EF Core                                           |
| Mensageria       | RabbitMQ · padrão outbox/inbox · workers assíncronos          |
| Observabilidade  | OpenTelemetry (OTel) · Grafana · Loki · Tempo · Prometheus    |
| Cloud & DevOps   | Docker · CI/CD · OCI (Oracle Cloud)                            |

## Projetos

### Ourivus

Plataforma operacional para o setor de **joalheria e ourivesaria**, voltada à venda
de peças personalizadas a partir de modelos 3D. O cliente envia um arquivo `.stl`,
customiza a peça e recebe preço e prazo calculados em tempo real; nos bastidores, a
plataforma cobre todo o ciclo — pagamento, fiscal e logística — em um fluxo único e
automatizado.

**Principais capacidades:**

- **Processamento 3D (STL):** upload de modelos, renderização assíncrona com
  validação geométrica e cálculo de volume, peso e preço.
- **Catálogo e precificação:** materiais (ouro, prata, aço), pacotes, promoções e
  cupons, com configuração operacional dinâmica.
- **Pedidos e checkout:** carrinho, endereços, cálculo de frete e confirmação.
- **Pagamentos:** integração com Mercado Pago (preferências e webhooks idempotentes).
- **Fiscal:** emissão e sincronização de NF-e via Bling/SEFAZ, com acesso protegido a XML/PDF.
- **Logística:** cotação, pré-postagem, etiquetas e rastreamento dos Correios.
- **Notificações:** e-mail e WhatsApp disparados por eventos do pedido.
- **Administração:** dashboard operacional, RBAC com permissões por funcionalidade e trilha de auditoria.

**Arquitetura:** backend .NET em Vertical Slice Architecture com CQRS,
EF Core + PostgreSQL e worker dedicado (RabbitMQ) para processamento 3D, fiscal e
notificações; frontend React com SSR e TypeScript.

### Loja BQZ

Plataforma de **e-commerce industrial** que unifica comercialização, operação e
fiscal de uma empresa do setor em um único sistema, atendendo tanto vendas **B2B**
quanto **B2C**. Combina catálogo técnico, ciclo de orçamento e expedição operacional
integrada.

**Principais capacidades:**

- **Catálogo industrial:** produtos e SKUs com variações, mídia, especificações
  técnicas, NCM e integração com ERP; categorias e coleções.
- **Vendas:** carrinho, orçamentos com pagamento de sinal e aprovação de
  vendedor, cupons e descontos administrativos.
- **Checkout e pagamentos:** cálculo de frete (Correios), Mercado Pago e endereços
  de entrega/cobrança.
- **Fiscal:** emissão e reconciliação de NF-e via Bling, cálculo de ICMS/DIFAL por
  estado e acesso protegido a documentos.
- **Expedição e picking:** fila de separação, pacotes, etiquetas ZPL (impressora
  térmica), declaração de conteúdo e rastreamento.
- **Estoque:** disponibilidade, reposição e transferência entre estoques.
- **Conteúdo e layout:** versões de layout, menus, banners, carrosséis, grids e
  páginas customizadas (CMS).
- **Acesso:** usuários, papéis e permissões granulares.

**Arquitetura:** construída sobre a mesma base do Ourivus — backend C#/.NET em
Vertical Slice Architecture, EF Core + PostgreSQL, padrão outbox/inbox com worker
dedicado para fiscal, pagamentos e expedição; frontend React com SSR; armazenamento
em OCI (Oracle Cloud) e observabilidade com OpenTelemetry.

### Credenciamento Machine

Plataforma de **credenciamento e controle de presença para eventos e operações**.
Permite credenciar colaboradores em cargos, dias, turnos e equipes, registrar
presença e gerar relatórios de credenciamento, presença e pagamento — substituindo o
controle manual em planilhas por um fluxo integrado e auditável.

**Principais capacidades:**

- **Eventos e cargos:** cargos reutilizáveis organizados em uma matriz de
  dias × turnos × equipes, com limites por turno.
- **Colaboradores:** cadastro com campos customizáveis e documentos, e importação
  em lote via planilha Excel.
- **Credenciamento:** individual por cargo ou em lote por planilha (com seleção da
  coluna de documento), com processamento parcial e relatório de erros por registro.
- **Check-in:** presença rápida em modo kiosk (QR/código) ou por link com token assinado.
- **Contratos:** modelos de contrato e assinatura eletrônica.
- **Relatórios:** credenciamento, presença e pagamento, com exportação para CSV/Excel.
- **Acesso:** permissões granulares por ação.

**Arquitetura:** backend C#/.NET (ASP.NET Core) com PostgreSQL e EF Core, upload via
presigned URL no OCI, processamento de planilhas e jobs agendados (Quartz); frontend
Next.js (React, App Router) com TypeScript; observabilidade com OpenTelemetry e Grafana.

## Contato

Site: **https://pilati.dev**
