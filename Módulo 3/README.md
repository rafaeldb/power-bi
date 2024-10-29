# processando_e_transformado_dados_com_powerBI
Bootcamp 2024 NTT DATA - Engenharia de Dados com Python
## Conclusão do desafio 3 – Processamento de Dados Simplificado com Power BI
### Diferenças de que devem ser analisadas ao utilizar o comando "mesclar consultas" e "acrescentar consultas"

Quando utilizamos o comando **mesclar consultas** iremos selecionar primeiramente a tabela que será a referência para este processo, e logo em seguida selecionaremos a tabela ao qual iremos agregar colunas à primeira tabela (tabela referência). Para que este processo possa ser validado é necessário que haja uma coluna em comum entre ambas as tabelas que estão envolvidas no processo. Contudo é primordial observar que caso as duas tabelas não possuam as mesmas quantidades de linha poderá no ato da fusão gerar celulas com o conteúdo **null** ou **vazio**.
Então, se a sua intensão é juntar dados de duas colunas distintas em uma, utilize a função **mesclar consultas**, pois utilizando esta função as novas células irão agrupar lateralmente a tabela referência.

![mesclar consultas](mesclar_consultas.png)

A função **acrescentar consultas** deve ser utilizada com muita cautela, pois neste processo não há necessidade de haver coluna em comum entre as duas tabelas para a agregação da informação, ao selecionar a primeira tabela, essa será a referência, e a tabela selecionada posteriormente terá as suas colunas ausentes na primeira tabela, incluida na mesma.
Neste momento foram construídas as colunas da tabela condensada que está sendo criada. Agora é que vem a parte importante, os dados da primeira tabela permanecerão conforme estão dispostos, e os dados da segunda tabela irão ser adicionados logos abaixo dos dados da primeira tabela.
Contudo, caso os campos das tabelas não sejam idênticos irá gerar uma tabela com muitos problemas, apresentando diversas células em **banco** e com **null**
Tome muito cuidado ao ultilizar esta função.

![acrescentar consultas](acrescentar_consultas.png)


Descrição do desafio módulo 3 – Processamento de Dados Simplificado com Power BI

1. Criação de uma instância na Azure para MySQL
2. Criar o Banco de dados com base disponível no github
3. Integração do Power BI com MySQL no Azure
4. Verificar problemas na base a fim de realizar a transformação dos dados

Diretrizes para transformação dos dados

1. Verifique os cabeçalhos e tipos de dados
2. Modifique os valores monetários para o tipo double preciso
3. Verifique a existência dos nulos e analise a remoção
4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente
5. Verifique se há algum departamento sem gerente
6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas
7. Verifique o número de horas dos projetos
8. Separar colunas complexas
9. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção
10. Neste processo elimine as colunas desnecessárias.
11. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.
12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores
13. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.
14. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir.
15. Agrupe os dados a fim de saber quantos colaboradores existem por gerente
16. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela
