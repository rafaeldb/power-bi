Bootcamp 2024 NTT DATA - Engenharia de Dados com Python

## Conclusão do desafio 3 – Processamento de Dados
### Diferenças "mesclar consultas" e "acrescentar consultas"

Mesclar consultas: Ao utilizar essa função, seleciona-se primeiramente uma tabela como referência e em seguida outra tabela para agregar suas colunas. É essencial que exista pelo menos uma coluna em comum entre as duas tabelas. Se as quantidades de linhas forem diferentes, isso pode resultar em células com valores null ou vazios na tabela resultante. Essa função organiza os dados lado a lado na tabela de referência.

Acrescentar consultas: Essa função deve ser usada com cautela, pois não requer colunas em comum entre as tabelas. A tabela de referência permanece inalterada e as colunas da segunda tabela são adicionadas abaixo da primeira. No entanto, se as colunas não forem idênticas, a tabela resultante pode ter várias células vazias ou com valores null, resultando em problemas organizacionais.
