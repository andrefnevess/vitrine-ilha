# Requisitos

## Requisitos funcionais

| ID | Requisito | Prioridade |
| --- | --- | --- |
| RF01 | Exibir a lista de negócios em cards com foto, nome, categoria e bairro | Alta |
| RF02 | Buscar negócios pelo nome | Alta |
| RF03 | Filtrar negócios por categoria | Alta |
| RF04 | Filtrar negócios por bairro, combinável com a categoria e a busca | Alta |
| RF05 | Exibir a página de detalhe de um negócio | Alta |
| RF06 | Abrir conversa no WhatsApp a partir do detalhe | Média |
| RF07 | Enviar um novo negócio pelo formulário de cadastro (envio simulado) | Média |
| RF08 | Preencher rua e bairro automaticamente a partir do CEP (ViaCEP) | Média |
| RF09 | Validar os campos obrigatórios do formulário | Média |

## Requisitos não funcionais

| ID | Requisito |
| --- | --- |
| RNF01 | Layout responsivo, de 375 px a 1440 px (mobile first) |
| RNF02 | Código em TypeScript, sem uso de `any` |
| RNF03 | Componentes reutilizáveis, um por pasta, com estilo em CSS Modules |
| RNF04 | Acesso a dados somente pela camada de serviço (`src/services`) |
| RNF05 | Acessibilidade básica: `alt` em imagens, `label` em campos e navegação por teclado |
| RNF06 | Mensagens claras para carregamento, lista vazia e erro |
| RNF07 | Deploy automático na Vercel a cada push na branch `main` |

## Regras de negócio

| ID | Regra |
| --- | --- |
| RN01 | O CEP deve ter 8 dígitos; a consulta só acontece quando os 8 estiverem preenchidos |
| RN02 | CEP inexistente (resposta `{ "erro": true }`) exibe mensagem e libera o preenchimento manual |
| RN03 | O WhatsApp é armazenado só com números, no formato 55 + DDD + número |
