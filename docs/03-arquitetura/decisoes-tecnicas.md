# Decisões Técnicas (ADRs)

Registro curto das decisões de arquitetura: contexto, decisão e consequência.

## ADR 001 — Vite + React + TypeScript

- **Contexto:** o projeto precisa de componentização e tipagem, com configuração simples.
- **Decisão:** usar Vite com o template `react-ts`.
- **Consequência:** build rápido e tipagem desde o início; sem renderização no servidor.

## ADR 002 — CSS Modules em vez de framework de CSS

- **Contexto:** o objetivo é demonstrar domínio de CSS e layout responsivo.
- **Decisão:** um arquivo `.module.css` por componente.
- **Consequência:** estilos isolados e CSS escrito à mão; mais código de estilo que com Tailwind.

## ADR 003 — Dados em JSON + camada de serviço

- **Contexto:** o MVP não tem backend, mas deve demonstrar consumo de API.
- **Decisão:** servir `public/data/businesses.json` e buscá-lo com `fetch` dentro de `src/services`.
- **Consequência:** o deploy continua estático; migrar para um banco (ex.: Supabase) altera só os serviços.

## ADR 004 — ViaCEP para endereço

- **Contexto:** o cadastro precisa de endereço e de uma integração com API pública real.
- **Decisão:** consultar `https://viacep.com.br/ws/{cep}/json/`.
- **Consequência:** é preciso tratar CEP inexistente e falha de rede.

_Novas decisões entram aqui com o próximo número._
