
# 🧊 Previsão de Vendas de Sorvete com Regressão Linear

[![Status](https://img.shields.io/badge/pipeline-completed-brightgreen)]()  
Projeto de machine learning desenvolvido no **Azure Machine Learning Studio** para prever a quantidade de **sorvetes vendidos** com base na **temperatura** utilizando **regressão linear**.



## 📈 Objetivo

Demonstrar a criação de um pipeline de regressão simples no Azure ML Studio para prever vendas de sorvete com base em dados históricos de temperatura.



## 🗂️ Dados Utilizados

O conjunto de dados utilizado se chama **`Sorvetes`**, contendo:

| Coluna               | Tipo     | Descrição                               |
|----------------------|----------|------------------------------------------|
| Temperatura          | Numérico | Temperatura registrada (ºC)             |
| Vendas de Sorvete    | Numérico | Quantidade de unidades vendidas         |



## 🧪 Pipeline Criado

Pipeline montado no Azure ML Studio:

```plaintext
 Dataset -> Select Columns -> Split Data
                                 |       |
      Linear Regression -> Train Model  |
                  |               |     |
                Score Model <------     |
                     |
                Evaluate Model
```

### Componentes Utilizados:
- `Select Columns in Dataset`
- `Split Data` (divisão treino/teste)
- `Linear Regression`
- `Train Model`
- `Score Model`
- `Evaluate Model`



## 📊 Avaliação do Modelo

Após treinar e testar o modelo de regressão linear, os seguintes resultados foram obtidos:

| Métrica                  | Valor      |
|--------------------------|------------|
| 🟢 Mean Absolute Error   | **13.204** |
| 🟢 Root Mean Squared Error | **15.813** |

### Observações:
- O modelo tende a prever valores próximos a **34.915**, com baixa variância.
- Isso pode indicar necessidade de ajustes como:
  - Adição de mais variáveis explicativas
  - Normalização dos dados
  - Teste com algoritmos mais complexos (Ex: árvores de decisão)



## 📂 Scored Dataset (Exemplo)

| Temperatura | Vendas Reais | Previsão do Modelo |
|-------------|--------------|--------------------|
| 32          | 57           | 37.24              |
| 35          | 16           | 34.91              |
| 26          | 42           | 41.89              |
| 24          | 39           | 43.45              |
| ...         | ...          | ...                |


## ✅ Etapas para criar novo grupo de recursos e configurar Azure Machine Learning:

1. Acesse o portal do Azure [https://portal.azure.com](https://portal.azure.com)
2. Pesquise por "Grupos de recursos" na barra de busca superior
3. Clique em “Criar” ou “+ Adicionar”
4. Preencha os campos:
   - Assinatura: selecione sua assinatura ativa
   - Nome do grupo de recursos: ex: ml-recursos-projeto
   - Região: escolha a mesma região que usará para o serviço de ML (ex: East US, Brazil South, etc)
5. Clique em “Revisar + criar” e depois em “Criar”

## 🔧 Agora, crie o workspace do Azure Machine Learning
6. Após o grupo de recursos ser criado, volte ao menu inicial e pesquise por "Azure Machine Learning"
7. Clique em "Criar" e selecione:
   - Grupo de recursos: o que você acabou de criar
   - Nome do workspace: ex: ml-workspace-sorvete
   - Região: a mesma do grupo de recursos
   - Tipo de armazenamento, key vault, etc: deixe como padrão se for um teste/projeto simples
8. Clique em “Revisar + criar”, e depois em “Criar”

## ▶️ Como Reproduzir no Azure ML Studio

1. Acesse [https://ml.azure.com](https://ml.azure.com)
2. Crie um novo **experimento (pipeline clássico)**.
3. Importe seu dataset `Sorvetes`.
4. Adicione os seguintes módulos na ordem:
   - Select Columns in Dataset
   - Split Data
   - Linear Regression
   - Train Model
   - Score Model
   - Evaluate Model
5. Execute o pipeline.
6. Visualize os resultados no módulo `Evaluate Model`.



## 📌 Próximos Passos

- [ ] Testar algoritmos como **Árvore de Regressão**, **Boosted Trees**, etc.
- [ ] Incluir outras variáveis (ex: dia da semana, feriados, promoções).
- [ ] Automatizar o pipeline com **MLflow** e **implantação em nuvem**.
- [ ] Gerar gráficos com visualizações interativas dos resultados.



## 👤 Autor

Desenvolvido por Henrique Poletti  
🔗 Interesse em MLOps, DevOps, Data Science e soluções em nuvem.  
📅 Experimento executado em **09 de Maio de 2025**


