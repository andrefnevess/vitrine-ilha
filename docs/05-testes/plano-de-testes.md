# Plano de Testes

Ferramentas: Vitest + Testing Library.

## Testes automatizados

| ID | O que testa | Tipo | Situação |
| --- | --- | --- | --- |
| T01 | `filterBusinesses` filtra por nome, categoria e bairro combinados | Unitário | Pendente |
| T02 | `BusinessCard` exibe nome, categoria e bairro recebidos por props | Componente | Pendente |
| T03 | `EmptyState` aparece quando a busca não tem resultado | Componente | Pendente |

## Testes manuais

| ID | Cenário | Resultado esperado | Situação |
| --- | --- | --- | --- |
| M01 | Abrir a vitrine em 375 px | Cards em uma coluna, sem rolagem horizontal | Pendente |
| M02 | Digitar um CEP válido | Rua e bairro preenchidos | Pendente |
| M03 | Digitar um CEP inexistente | Mensagem de CEP não encontrado | Pendente |
| M04 | Navegar só com o teclado | Todos os elementos alcançáveis, foco visível | Pendente |
| M05 | Acessar uma rota inexistente | Página "não encontrada" com link para a vitrine | Pendente |
