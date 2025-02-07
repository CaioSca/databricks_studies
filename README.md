# Databricks Studies

sources: https://www.youtube.com/watch?v=9yKecTXW2pY, https://www.youtube.com/watch?v=x1mXZlllQmw&list=PLz-qytj7eIWXTqncmCCSOw-GcBu2c4K0j&index=23

- Principalmente uma ferramenta pra atuar com o armazenamento/processamento de big data (mas não só)
- Possui spark embutido, para processamento eficiente, bem como as delta tables, otimizadas para leitura e escrita e com suporte para acid
![image](https://github.com/user-attachments/assets/09d17c20-30bd-4d7d-81bf-bbf39a2354d7)


![image](https://github.com/user-attachments/assets/9a43455b-38be-42da-aa5e-22b48e1c47ce)
- Interação com o serviço pode se dar através de CLI / SDK (com python, por ex.) / API / Web UI
- Possui funcionalidades como a de orquestração, catalagoção, armazenamento de queries, códigos e modelos de ML, permissionamento granular, storage próprio e diferentes (4) formas de computação

- workspaces e notebooks ficam conectados a clusters específicos e tem seus dbfs próprios


# Secrets
- configurável através da CLI ou da própria Azure
- instalar CLI do databricks
- databricks configure, para vincular à sua conta
- databricks secrets create-scope [nome], para criar o escopo (específico) que vai abrigar seus secrets (específicos)
- databricks secrets put secret [scope] [nome da key] [--flag, que é basicamente a forma de armazenar o valor, ex.: --string-value] [valor]
- pronto, segredo adicionado
- para utilizar o segredo, basta, no seu notebook, usar dbutils.secret.get([scope], [key])
