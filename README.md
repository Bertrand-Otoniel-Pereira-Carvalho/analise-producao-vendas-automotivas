# Análise de Produção e Vendas Automotivas

Dashboard em Power BI para análise de produção e vendas de veículos, cruzando indicadores por modelo de veículo, região (sede, gerência, cidade) e período. Construído com modelagem em esquema estrela e medidas DAX.

## Problema de negócio

[PREENCHER: descreva em 2-3 frases a pergunta de negócio que motivou o dashboard — ex.: "A empresa precisava entender se o volume de produção estava alinhado à demanda de vendas por região e modelo de veículo, e identificar onde havia gargalos ou excedentes."]

## Estrutura dos dados

O modelo segue um esquema estrela, com uma tabela fato e dimensões de apoio:

- **`f_Produção`** (fato) — registros de produção e vendas
- **`d_Veículo`** — dimensão de modelos de veículo
- **`d_Local`** — dimensão de localização (sede, gerência, cidade)
- **`d_Preços`** — dimensão de preços/valores unitários
- **`d_calendário`** — dimensão de tempo
- **`d_atualização`** — controle da data de última atualização dos dados
- **`_Medidas`** — tabela dedicada às medidas DAX do relatório

## Estrutura do dashboard

O relatório tem 3 páginas:

### 1. Resumo
Visão executiva com cards de KPI, tabela dinâmica de vendas, produção total por ano e veículo, evolução do preço médio unitário por ano e veículo, e funis comparando venda e produção por modelo. Filtros por sede, modelo, gerência, cidade e data.

![Página Resumo](images/pagina-resumo.png)

### 2. Análise de Dados
Aprofundamento com funis complementares, gráfico de área empilhada mostrando evolução no tempo, e um mapa geográfico com a produção mapeada por localização.

![Página Análise de Dados](images/pagina-analise-dados.png)

### 3. Decomposição Venda/Produção
Duas árvores de decomposição interativas, permitindo detalhar o total de vendas e o total de produção por qualquer combinação de dimensões (veículo, local, período).

![Página Decomposição](images/pagina-decomposicao.png)

## Principais insights

[PREENCHER: liste de 3 a 5 descobertas concretas que o dashboard revelou, por exemplo:]
- [PREENCHER: ex. "O modelo X respondeu por Y% da produção total, mas apenas Z% das vendas no período, indicando possível excesso de estoque."]
- [PREENCHER: ex. "A região X apresentou o maior preço médio unitário, enquanto a região Y teve o maior volume de vendas."]
- [PREENCHER: ex. "Observou-se sazonalidade na produção entre os meses X e Y."]

## Tecnologias utilizadas

- **Power BI Desktop** — modelagem, visualizações e publicação
- **DAX** — medidas calculadas (tabela `_Medidas`)
- **Modelagem dimensional** — esquema estrela (fato + dimensões)
- **Power Query** — tratamento e transformação dos dados de origem

## Como visualizar

- Arquivo original: [`dashboard.pbix`](./dashboard.pbix) — abra no Power BI Desktop (gratuito) para navegar de forma interativa
- Versão estática: [`relatorio.pdf`](./relatorio.pdf) — para visualização rápida sem precisar instalar o Power BI

## Autor

**Bertrand Otoniel Pereira Carvalho**
[LinkedIn](https://www.linkedin.com/in/bertrandotoniel) · [GitHub](https://github.com/Bertrand-Otoniel-Pereira-Carvalho)
