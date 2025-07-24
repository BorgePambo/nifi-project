Descrição do Fluxo NiFi
Este projeto contém um fluxo de ETL construído com Apache NiFi, cujo objetivo é ler arquivos locais, processar os dados e armazená-los em um banco de dados relacional (MySQL). O fluxo segue as seguintes etapas principais:

🔄 Etapas do Fluxo:
GetFile
Lê arquivos de uma pasta local especificada no container NiFi.
          
          UpdateAttribute
          Atualiza atributos do FlowFile, como nome do arquivo, encoding, ou outras informações necessárias para o processamento.
          
          ConvertRecord
          Converte os dados de entrada (ex: CSV ou JSON) para um formato estruturado, utilizando um Record Reader (ex: CSVReader) e Record Writer (ex: JSONRecordSetWriter).
          
          QueryRecord
          Executa transformações SQL-like nos registros do FlowFile, como filtros, joins ou alterações de colunas.
          
          PutDatabaseRecord
          Insere os dados processados diretamente no banco de dados MySQL, utilizando um DBCPConnectionPool para gerenciar a conexão com o banco.
          
          ⚙️ Tecnologias utilizadas
          Apache NiFi 2.4.0
          
          MySQL (via container Docker)

          Docker Compose
          
          Driver JDBC MySQL 8.0.23




