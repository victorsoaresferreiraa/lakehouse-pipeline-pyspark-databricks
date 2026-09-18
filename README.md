# Pipeline de Engenharia de Dados em Lakehouse (PySpark & Delta Lake)

Projeto prático de engenharia de dados implementado no **Databricks**, estruturado segundo a **Arquitetura Medalhão** para processamento e modelagem de dados de transporte.

## 📌 Arquitetura do Pipeline

O fluxo segue o padrão Lakehouse em três camadas:

1. **Bronze (Dados Brutos):** Ingestão de dados de transporte e persistência no formato transacional Delta Lake sem modificações estruturais.
2. **Prata (Limpeza e Padronização):** Padronização de esquemas (`snake_case`), tratamento de nulos/duplicatas e criação de métricas derivadas (`categoria_demanda`).
3. **Ouro (Consumo Analítico):** Agregações anuais para consumo direto de ferramentas de BI e tomada de decisão executiva.

## 🛠️ Tecnologias Utilizadas

* **Databricks Serverless** (Ambiente de processamento distribuído)
* **Apache Spark / PySpark** (ETL distribuído)
* **Delta Lake** (Camada de armazenamento ACID e Time Travel)
* **Python / Pandas** (Ingestão de fontes externas)

## 🔍 Diferenciais Técnicos Aplicados

* **ACID Transactions:** Gravação consistente em formato Delta em todas as camadas.
* **Governança e Auditoria:** Rastreabilidade de alterações via logs de transação com `DESCRIBE HISTORY`.
* **Time Travel:** Capacidade de restauração e consulta de versões históricas das tabelas.
