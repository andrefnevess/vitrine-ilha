# Vitrine Ilha — Pequenos Negócios de São Luís

Catálogo web onde moradores de São Luís (MA) encontram pequenos negócios por categoria e bairro, e onde empreendedores podem enviar o próprio negócio para aparecer na vitrine.

> **Status do projeto:** Sprint 0 — Planejamento e design

**Deploy:** _em breve_ · **Design (Figma):** _em breve_

---

## Sobre o Projeto

### Problema

Muitos pequenos negócios de São Luís dependem só do boca a boca e de perfis soltos em redes sociais. Quem procura um serviço no próprio bairro não tem um lugar simples para descobrir essas opções.

### Objetivo

Construir uma interface web responsiva, organizada em componentes e tipada com TypeScript, que consome dados por uma camada de serviço e integra uma API pública (ViaCEP).

### Público-alvo

- Moradores que procuram negócios locais por categoria ou bairro;
- Pequenos empreendedores que querem divulgar o próprio negócio.

## Funcionalidades (MVP)

| Módulo | Descrição |
| --- | --- |
| Vitrine | Lista de negócios em cards, com foto, nome, categoria e bairro |
| Busca e filtros | Busca por nome e filtros combináveis por categoria e bairro |
| Detalhe | Descrição, horário, endereço e contato por WhatsApp |
| Cadastro | Formulário com preenchimento de endereço pelo CEP (ViaCEP) |
| Estados de interface | Carregando, lista vazia e erro em todas as telas com dados |

Fora do MVP: login, avaliações, mapa e painel do empreendedor.

## Tecnologias

| Área | Tecnologia | Motivo |
| --- | --- | --- |
| Base | Vite + React | Projeto rápido de configurar, componentização |
| Linguagem | TypeScript | Tipagem de dados, props e funções |
| Rotas | React Router | Navegação entre vitrine, detalhe e cadastro |
| Estilo | CSS Modules | Estilo isolado por componente, layout responsivo |
| Dados | fetch + camada de serviço | Componentes desacoplados da origem dos dados |
| API externa | ViaCEP | Consulta de endereço pelo CEP |
| Testes | Vitest + Testing Library | Testes de componentes e funções |
| Design | Figma | Telas para celular e desktop antes do código |
| Deploy | Vercel | Publicação automática a cada push |

As decisões técnicas estão registradas em [`docs/03-arquitetura/decisoes-tecnicas.md`](docs/03-arquitetura/decisoes-tecnicas.md).

## Arquitetura

Aplicação front-end de página única (SPA). As páginas usam hooks, os hooks chamam a camada de serviço e a camada de serviço busca os dados (arquivo JSON servido pelo site e API ViaCEP). Ver [`docs/03-arquitetura/arquitetura.md`](docs/03-arquitetura/arquitetura.md).

## Metodologia

Kanban individual com sprints curtas de um dia, usando GitHub Issues e Projects. Cada funcionalidade vira uma issue e é entregue por um pull request. Ver [`docs/04-gestao/roadmap.md`](docs/04-gestao/roadmap.md).

## Estrutura do Repositório

```
.
├── README.md
├── LICENSE
├── .gitignore
├── .github/                 Modelos de issues e pull requests
├── docs/
│   ├── 01-produto/          Visão do produto e requisitos
│   ├── 02-design/           Telas, identidade visual e link do Figma
│   ├── 03-arquitetura/      Arquitetura e decisões técnicas (ADRs)
│   ├── 04-gestao/           Roadmap e backlog
│   └── 05-testes/           Plano e casos de teste
├── public/
│   └── data/                Dados fictícios dos negócios (JSON)
└── src/                     Código da aplicação (a partir da Sprint 1)
    ├── components/          Componentes reutilizáveis
    ├── pages/               Páginas (Vitrine, Detalhe, Cadastro)
    ├── services/            Acesso a dados e APIs
    ├── hooks/               Hooks customizados
    ├── types/               Tipos TypeScript
    └── utils/               Funções auxiliares
```

## Como Executar

> Em elaboração. As instruções serão completadas quando o primeiro incremento estiver disponível.

Pré-requisitos: Node.js (versão LTS) e Git.

```bash
git clone https://github.com/andrefnevess/vitrine-ilha.git
cd vitrine-ilha
npm install
npm run dev
```

## Status do Projeto

| Entrega | Situação |
| --- | --- |
| Estrutura do repositório | Concluída |
| Visão do produto e requisitos | Concluída |
| Design no Figma | Não iniciado |
| Vitrine com busca e filtros | Não iniciado |
| Página de detalhe | Não iniciado |
| Cadastro com ViaCEP | Não iniciado |
| Testes | Não iniciado |
| Deploy na Vercel | Não iniciado |

## Sobre os Dados

Os negócios exibidos são **fictícios** e servem apenas para demonstração. Nenhum negócio real é publicado sem autorização do responsável.

## Autor

**André Neves** — Estudante de Engenharia de Software (UNDB)
[LinkedIn](https://www.linkedin.com/in/andrefneves/) · [Portfólio](https://portfolionewandreneves.vercel.app/) · [GitHub](https://github.com/andrefnevess)

## Licença

Distribuído sob a licença MIT. Ver [`LICENSE`](LICENSE).
