# Data Mart - Marketing - Pentaho PDI
Este projeto tem como objetivo criar um Data Mart para area de Marketing fazer as analises de vendas. Utilizando a abordagem direta, o Pentaho Data Integration (PDI) é utilizado para realizar a extração, transformação e carga (ETL) dos dados diretamente para o Data Mart, sem a etapa intermediária de stage.

Ao utilizar a abordagem direta, eliminamos a etapa de stage, o que pode resultar em ganhos de desempenho e redução de complexidade no processo de ETL. No entanto, fizemos uma analise minuciosa na qualidade dos dados extraídos e a consistência das transformações realizadas, garantindo que o Data Mart seja alimentado com informações confiáveis e precisas.

Para a criação do modelo multidimensional do Data Mart, foi escolhido o modelo Estrela, pois é implementado em banco de dados relacional, facilitando a implementação e também por utilizar linguagem SQL para a consulta dos dados. O SGBD escolhido foi o MySQL versão 8.0.33, um banco de dados opensource amplamente utilizado no mercado.

## Requisitos
* Pentaho Data Integration (PDI) - versão 9.3 
* PostgreSQL - versão 15.2
* MySQL - versão 8.0.33

## Arquitetura do Projeto
O projeto é composto por três principais etapas:

1 - **Extração**: Os dados são extraídos diretamente do banco de dados PostgreSQL, que é a fonte de dados principal. As tabelas relevantes são selecionadas e os dados são transferidos para o processo de transformação direto no data mart.<br>
2 - **Transformação**: Nesta etapa, os dados extraídos são transformados e isso inclui limpeza, padronização, cálculos e criação de tabelas fato e dimensões.<br>
3 - **Carga no Data Mart**: Após a transformação dos dados, eles são carregados diretamente no data mart. O processo de carga é realizado por meio de um job do PDI, que executa a transformação e atualiza as tabelas do data mart.<br>

## Estrutura do Repositório
***/documentacao**: Contém o backup do Data Mart.<br>
***/etl**: Armazena a pasta zipada com os arquivos ktr (transformação) e kjb (Job) do PDI para as etapas de ETL.<br>
***/scripts**: Inclui a base de dados em linguagem SQL para configuração do banco de dados e otimizações.<br>

## Configuração e Execução do Job
1 - Instale o Pentaho Data Integration (PDI),o PostgreSQL e o MySQL em seu ambiente.<br>
2 - Configure a conexão com os dois bancos de dados diretamente no PDI, fornecendo as informações de acesso de cada banco de dados.<br>
3 - No PDI, execute arquivo job_Principal.kjb para realizar a carga dos dados transformados no data mart.<br>

![image](https://github.com/thuanyvermelho/Data_Warehouse_Pentaho/assets/104110519/ff679fc3-ed1f-48d1-b01e-a0c85f3417dc)

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para enviar pull requests com melhorias, correções de bugs ou novas funcionalidades.
