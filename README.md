

---

# MVP – Engenharia de Dados

Este repositório contém o **MVP desenvolvido para a disciplina de Engenharia de Dados**, cujo objetivo é demonstrar a aplicação prática de conceitos de **ingestão, transformação, modelagem, qualidade de dados e análise analítica**, utilizando um ambiente de dados em nuvem (Databricks).

O projeto cobre todo o **ciclo de vida dos dados**, desde a coleta até a geração de insights de negócio, seguindo boas práticas de arquitetura e governança de dados aprendidas na disciplina. 

O "Readme" propõe somente passar uma visão resumida do que foi feito no databricks. Junto a esse documento, foi feito o upload de dois arquivos, o primeiro de formato HTML para uma versão completa do notebook exportada do Databricks e uma ipynb que permite a visualização direta pelo direta no GitHub. Adicionalmente, como evidência, subirei o arquivo HTML no site da pós juntamente com o link do repositório do Github. Nesses arquivos será possível identificar todo o trabalho feito de código, difículdades e processos de decisão

---

## Objetivo do Projeto

Analisar dados de vendas de uma rede varejista fictícia (**DT Mart**) com foco em:

* Evolução das vendas ao longo do tempo (série temporal)
* Identificação de tendências e sazonalidade
* Avaliação do impacto de preços e promoções sobre vendas e receita
* Validação da qualidade dos dados utilizados nas análises

---

## Fonte dos Dados

* **Origem:** Kaggle
* **Dataset:** DT MART – Market Mix Modeling
* **Tipo:** Dados sintéticos com estrutura realista
* **Conteúdo:** vendas, preços, promoções, investimento em mídia e indicadores de mercado

Os dados são públicos e foram utilizados respeitando princípios éticos e acadêmicos.

---

## Arquitetura de Dados

O projeto segue a **Metodologia Medalhão**, utilizada em arquiteturas de dados:

### Camada Bronze

* Dados brutos carregados diretamente no Databricks
* Estrutura original preservada
* Sem transformações ou limpezas

### Camada Prata

* Limpeza, padronização e tipagem dos dados
* Tratamento de datas, valores nulos e tipos numéricos
* Integração entre múltiplas fontes
* Construção do pipeline ETL em PySpark

### Camada Ouro

* Modelagem analítica em **Esquema Estrela**
* Criação da **Tabela Fato de Vendas**
* Criação das **Dimensões Produto e Tempo**
* Catálogo de dados e validação de qualidade
* Base pronta para análises e tomada de decisão

---

## Modelagem Analítica

* **Fato:** `fato_vendas_dw`
* **Dimensões:**

  * `dim_produto_dw`
  * `dim_tempo_dw`

A modelagem permite análises eficientes por produto, período, promoções e indicadores de mercado.

---

## Qualidade de Dados

Foi realizada uma análise formal de qualidade de dados (**Item 5.a do enunciado**), avaliando:

* Percentual de valores nulos por atributo
* Valores inválidos ou fora do domínio esperado
* Verificação de outliers
* Impacto dos dados na análise de negócio

Os resultados indicam **alta consistência e confiabilidade** da base analítica.

---

## Análises Realizadas (Item 5.b)

* Série temporal de vendas por semana e por mês
* Análise de sazonalidade
* Comparação entre períodos promocionais e não promocionais
* Avaliação do impacto das promoções sobre volume e receita

**Principais insights:**

* Não há tendência clara de crescimento ou queda no período analisado
* A sazonalidade é discreta, com leve aumento no fim do ano
* Promoções aumentam a **receita média**, mas não alteram significativamente o volume médio vendido

---

## Tecnologias Utilizadas

* Databricks
* Apache Spark (PySpark)
* SQL
* Delta Lake
* Python
* Jupyter Notebook

---

## Estrutura do Repositório

```
├── notebooks/
│   ├── MVP_Engenharia_Dados_DT_MART.ipynb
│   └── MVP_Engenharia_Dados_DT_MART.html
│
├── README.md
```

* `.ipynb`: visualização direta no GitHub
* `.html`: versão completa do notebook exportada do Databricks

---

## Autor

**Julio Cesar Losa**

