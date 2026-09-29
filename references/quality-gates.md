# Quality gates proporcionais

Escolha verificações a partir da alteração e da configuração do projeto. Registre comando, ambiente e resultado.

| Mudança | Verificação principal |
| --- | --- |
| Regra de negócio | Comportamento esperado e casos limite |
| Persistência ou migração | Integridade de dados, compatibilidade e caminho de reversão |
| Interface | Fluxo principal, estado de erro e viewport relevante |
| Empacotamento | Build e execução no sistema operacional alvo |
| Segurança ou autenticação | Acesso permitido e negado, sessão, segredos e integração |

Use linters e verificadores de tipo quando fizerem parte da stack. Meça a linha de base antes de tornar regras mais rígidas. Não imponha teto universal de linhas. Uma falha em gate obrigatório impede declarar aquela etapa concluída; relate falhas preexistentes com evidência separada.
