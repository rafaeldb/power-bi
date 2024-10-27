## Desafio de Modelagem e Transformação com DAX

As tabelas que constituem os bancos de dados são importadas para o Power BI replicando a estrutura constituída na sua construção, onde na maioria das vezes refere-se a um **banco de dados relacional**, porém por questão de obter melhor performance, utilizamos o modelo **star schema**, sendo necessário na re-estruturação na comunicação entre as tabelas **dimensão** e **fato**, criar novos relacionamentos para que possamos manter a fidelização dos dados.
Outro ponto que deve ser observado para que se mantenha a fluidez do relatório é sempre que possível fazer uso do **DAX** utilizando os comandos de **nova medida** e **medida rápida**, que impactará no tamanho do arquivo e velocidade de processamento. Como o uso da DAX não gera uma coluna numérica, não é possível realizar formatação através do **power query**.
Para desenvolver esta atividade do desafio foi construído além das tabelas convencionais a tabela **d_Calendário** no formato **DAX** para dar granulariadade e temporalidade ao processo de extração de dados. 


![Relacionamento Star Schema do Desafio Modelagem e Transformação com DAX]()
Desafio Modelagem e Transformação com DAX.png
