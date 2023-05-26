# Data Warehouse - Pentaho PDI
Este projeto tem como objetivo criar uma Data Warehouse para análise das vendas de veiculos. Utiliza o Pentaho Data Integration (PDI) para extrair, transformar e carregar os dados, seguindo as regras de negócios estabelecidas.

## Requisitos
* Pentaho Data Integration (PDI) - versão 9.3 
* PostgreSQL - versão 15.2
* MySQL - versão 8.0.33

## Arquitetura do Projeto
O projeto é composto por três principais etapas:

1 - **Extração**: Os dados são extraídos diretamente do banco de dados PostgreSQL, que é a fonte de dados principal. As tabelas relevantes para as vendas online de carros são selecionadas e os dados são transferidos para o processo de transformação.<br>
2 - **Transformação**: Nesta etapa, os dados extraídos são transformados de acordo com as regras de negócios estabelecidas. Isso inclui limpeza, padronização, cálculos e criação de tabelas fato e dimensões.<br>
3 - **Carga no Data Warehouse**: Após a transformação dos dados, eles são carregados diretamente no data warehouse. O processo de carga é realizado por meio de um job do PDI, que executa a transformação e atualiza as tabelas do data warehouse.<br>

## Estrutura do Repositório
***/documentacao**: Contém o backup do Data warehouse.<br>
***/etl**: Armazena os arquivos KTR e JOB do PDI para as etapas de ETL.<br>
***/scripts**: Inclui a base de dados em linguagem SQL para configuração do banco de dados e otimizações.<br>

## Configuração e Execução do Job
1 - Instale o Pentaho Data Integration (PDI),o PostgreSQL e o MySQL em seu ambiente.<br>
2 - Configure a conexão com os dois bancos de dados diretamente no PDI, fornecendo as informações de acesso.<br>
3 - No PDI, execute arquivo job_Principal.kjb para realizar a carga dos dados transformados no data warehouse.<br>


## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para enviar pull requests com melhorias, correções de bugs ou novas funcionalidades.
