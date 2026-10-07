# Arquitetura

Aplicação front-end de página única (SPA), sem backend próprio.

## Fluxo de dados

```
Página  →  Hook  →  Serviço  →  Fonte de dados
(Home)     (useBusinesses)  (businessService)  (public/data/businesses.json)
(Register) (useCep)         (cepService)       (API ViaCEP)
```

- **Páginas** montam a tela e combinam componentes.
- **Hooks** guardam o estado da busca (dados, carregando, erro).
- **Serviços** são o único lugar que faz `fetch`. Trocar a fonte de dados muda só esta camada.
- **Componentes** recebem dados por props e não sabem de onde eles vêm.

## Modelo de dados

```ts
export type Category = 'Alimentação' | 'Moda' | 'Beleza' | 'Serviços' | 'Artesanato';

export interface Business {
  id: string;
  name: string;
  category: Category;
  neighborhood: string;
  description: string;
  whatsapp: string;
  hours: string;
  imageUrl: string;
}
```

## Rotas

| Rota | Página |
| --- | --- |
| `/` | Vitrine |
| `/negocio/:id` | Detalhe |
| `/cadastrar` | Cadastro |
| `*` | Página não encontrada |
