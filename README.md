# Amostra de testes funcionais de aplicação web

Demonstração independente realizada em **09/10/2026** no aplicativo público [Swag Labs](https://www.saucedemo.com/). Esta amostra mostra o formato de documentação de um ciclo pequeno de testes. Não representa um serviço anterior para cliente.

## Escopo e ambiente

Interface desktop observada no navegador integrado do Codex. Foram verificados seis cenários de autenticação, catálogo e carrinho, usando a conta pública de demonstração informada pelo próprio aplicativo. Não houve compra finalizada, pagamento ou uso de dados pessoais reais.

## Resultados

| ID | Ação e resultado esperado | Comportamento observado | Resultado |
|---|---|---|---|
| QA01 | Clicar Login com os campos vazios; impedir autenticação e pedir usuário | Mensagem `Username is required`; permaneceu no login | Passou |
| QA02 | Entrar com a conta padrão pública; abrir catálogo | Navegou para `inventory.html` com produtos | Passou |
| QA03 | Selecionar preço crescente; apresentar valores não decrescentes | 7,99; 9,99; 15,99; 15,99; 29,99; 49,99 | Passou |
| QA04 | Adicionar Backpack; conferir item, quantidade e preço no carrinho | Carrinho com um Backpack, quantidade 1, preço 29,99 | Passou |
| QA05 | Remover Backpack; esvaziar carrinho e contador | Carrinho vazio; nenhum item listado | Passou |
| QA06 | Menu > Logout; voltar ao formulário de login | Página raiz com campos de login | Passou |

Cinco capturas de tela foram preservadas no registro local da execução: login vazio, ordenação, carrinho, carrinho vazio e logout. As imagens não estão publicadas neste repositório. O login bem-sucedido foi documentado pelo estado da interface e corroborado pela captura da ordenação.

## Limitações

Nenhuma falha foi encontrada nesses seis cenários. Isso não prova ausência de bugs no aplicativo. Não foram testados persistência de sessão após logout, dispositivos móveis, segurança, acessibilidade completa ou integração Azure DevOps.

Um relatório com falhas deve registrar passos de reprodução, resultado esperado e observado e evidência. Esta amostra não inventa defeitos para demonstrar esse formato.

## Aplicação em um serviço

Um ciclo contratado deve ter ambiente autorizado, fluxos prioritários e critérios de aceite definidos antes do início. Esta publicação não constitui proposta vinculante, certificação de qualidade, promessa de cobertura completa ou oferta de teste sobre sistemas sem autorização.
