https://www.youtube.com/watch?v=D5mwXMMA0e0&ab_channel=ProgramadorLhama

## ETL Pipeline - Introdução

- Sistema que tem a capacidade de ler diferentes formatos de arquivos e tipos de dados, e transportá-los de um ambiente para outro.
- Tipo de Data Integration em três etapas usado para combinar (mover e transformar) dados de diversas fontes e carregá-los em vários destinos.
- Comumente utilizado para construir um **Data Warehouse**.

**Processos/Estágios de ETL**
* Extração
* Transformação (ou Limpeza)
* Carga de Dados (ou Entrega, ou Carregamento)

[![](https://blog.gft.com/br/wp-content/uploads/sites/4/2016/09/Etl.jpg)](https://blog.gft.com)
*Os dados são retirados (extraídos) de um sistema-fonte, convertidos (transformados) em um formato que possa ser analisado, e armazenados (carregados) em um armazém ou outro sistema.*

**O que é um pipeline de Dados**

- É uma *série* de etapas de processamento de dados.
    - **De outra forma**: É um *fluxo de processamento de dados* divididos em *etapas sequenciais*.
    - **Processamento de Dados**: conjunto de operações realizadas sobre dados brutos para transformá-los em informações úteis.
        - Essas operações podem incluir coleta, organização, armazenamento, análise e apresentação dos dados.
- A saída de uma fase/etapa serve como entrada para a próxima.
- Etapas independentes podem ser executadas em paralelo.
- Consiste em três elementos principais:
    - fonte
    - etapas de processamento
    - destino/coletor
- Podem ter a mesma fonte e coletor.
    - Nesse caso, o pipeline serve apenas para modificar o conjunto de dados.
    - **Exemplo 1**: Imagine um sistema bancário que armazena informações de transações.
        - Os dados vêm do banco de dados principal (Ponto A).
        - Um pipeline de dados processa e formata os dados (exemplo: converte moedas, remove duplicatas, ajusta erros).
        - O conjunto modificado é salvo de volta no mesmo banco de dados (Ponto A).
        - *Aqui, o pipeline apenas transforma os dados, sem alterar a fonte ou o coletor*.
    - **Exemplo 2**: pense em um pipeline que pega dados de um sensor de temperatura e os envia para diferentes destinos:
        - **Ponto A**: Sensor coleta dados.
        - **Ponto B**: Um sistema de monitoramento recebe os dados.
        - **Ponto C**: Uma IA analisa padrões climáticos.
        - **Ponto D**: Um app exibe gráficos para o usuário.
        - *Neste caso, o pipeline de dados conecta vários pontos, movendo e processando informações entre eles*.

**Diferença entre ETL e Pipeline**
- **ETL e Pipeline de Dados não são a mesma coisa**.
- ETL (Extract, Transform, Load) é um processo tradicional de movimentação de dados que ocorre em três fases:
    - 1️⃣ Extract (Extração): Coleta dados de uma ou mais fontes (bancos de dados, APIs, planilhas, etc.).
    - 2️⃣ Transform (Transformação): Modifica os dados (limpeza, agregação, conversões, etc.).
    - 3️⃣ Load (Carga): Salva os dados transformados em um destino, como um Data Warehouse.
- Concentra-se apenas em extrair, transformar e carregar dados em um sistema de armazenamento de dados específico.
- **É apenas um dos componentes de um pipeline de dados**.
- **Pipeline é um conceito mais amplo. Ele representa qualquer fluxo automatizado de dados entre sistemas, podendo incluir ou não ETL.**
    - **Exemplo**: Uma loja online pode ter um pipeline que:
        - ✔ Coleta dados de compras em tempo real.
        - ✔ Envia os dados diretamente para um sistema de recomendação de produtos.
        - ✔ Atualiza os dados do usuário no banco de dados.
    - 🔹 Características principais do Pipeline de Dados:
        - ✅ Pode ser em tempo real ou em lotes.
        - ✅ Pode incluir ETL, ELT, streaming de dados, automações, etc.
        - ✅ O foco é no fluxo contínuo de dados entre sistemas.

| **ETL** | **Pipeline de Dados** |
|---------------------------------------|---------------------------------------------|
| Processo específico de **extração, transformação e carga** de dados. | Conceito mais amplo que representa qualquer fluxo de dados entre sistemas. |
| **Geralmente em lotes** (não em tempo real). | **Pode ser em tempo real** (ex.: streaming de dados). |
| **Foco na estruturação dos dados** antes de armazenar. | **Foco no movimento dos dados**, podendo incluir ou não transformação. |
| Normalmente leva os dados para um **Data Warehouse**. | Pode conectar diferentes sistemas, bancos de dados, APIs, etc. |
| Exemplo: Carregar dados tratados em um banco central para análise. | Exemplo: Transferir dados de um sensor IoT para um painel em tempo real. |


## Referências Bibliográficas
* https://www.sas.com/pt_br/insights/data-management/o-que-e-etl.html
* https://blog.dsacademy.com.br/mas-afinal-o-que-e-pipeline-de-dados/
* https://www.zendesk.com.br/blog/o-que-e-etl/