# Previsão de Produção de H2 Verde

Este repositório contém o código e a documentação de um projeto voltado para a predição da produção de H2 verde a partir de dados meteorológicos coletados de quatro estações localizadas no Ceará. O foco principal é prever a radiação solar e, a partir de modelos físicos, inferir a produção de H2.

## Contexto

O projeto abrange as seguintes etapas:
- **Pré-processamento dos Dados**: Tratamento de outliers, dados faltantes e outras inconsistências.
- **Análise Exploratória dos Dados (EDA)**: Obtenção de insights e compreensão dos dados pré-processados.
- **Visualização**: Geração de mapas com a localização das estações.
- **Otimização de Hiperparâmetros**: Uso de random search para identificar os melhores parâmetros para os modelos.
- **Predição**: Utilização dos melhores hiperparâmetros para realizar a predição da radiação solar e, consequentemente, estimar a produção de H2 verde.
- **Modelos Específicos**: Implementação de modelos SARIMA/SARIMAX para análises específicas.

## Estrutura do Repositório

```
config/
docs/
input/
output_forecast/
output_loc_data/
output_missing_data/
output_preprocessing/
data_preprocessing_jaguaribe.ipynb
data_preprocessing_jaguaruana.ipynb
data_preprocessing_sobral.ipynb
data_preprocessing_taua.ipynb
eda_jaguaribe.ipynb
eda_jaguaruana.ipynb
eda_sobral.ipynb
eda_taua.ipynb
map_stations.ipynb
prediction_jaguaribe.ipynb
prediction_jaguaruana.ipynb
prediction_sobral.ipynb
prediction_taua.ipynb
random_search_dl_sobral.ipynb
random_search_ml_sobral.ipynb
svr_random_search_analysis.ipynb
sarima_sobral.ipynb
sarimax_sobral.ipynb
```

### Pastas

- **config/**: Contém arquivos de configuração com variáveis globais, como o nome das estações, que são utilizadas para parametrizar os scripts de cada estação.
- **docs/**: Documentação técnica e referências relacionadas ao projeto.
- **input/**: Dados de entrada, incluindo dados meteorológicos e informações de localização das estações.
- **output_forecast/**: Resultados das predições e outputs dos experimentos de random search. A ser criado ao rodar os arquivos de Random Search
- **output_loc_data/**: Saídas referentes à geração de mapas com a localização das estações.
- **output_missing_data/**: Resultados iniciais da busca por dados faltantes.
- **output_preprocessing/**: Dados que passaram pelo processo de pré-processamento.

### Notebooks

- **data_preprocessing_<estacao>.ipynb**: Realizam o pré-processamento dos dados (tratamento de outliers, dados faltantes, etc.) para cada estação.
- **eda_<estacao>.ipynb**: Executam a Análise Exploratória dos Dados (EDA) a partir dos dados pré-processados.
- **map_stations.ipynb**: Gera mapas com a localização das estações utilizando os dados disponíveis em `input/`.
- **prediction_<estacao>.ipynb**: Realizam as predições utilizando os melhores hiperparâmetros identificados no random search.
- **random_search_<tecnica>_sobral.ipynb**: Notebooks que executam a seleção de features, preparação dos dados (incluindo time delay embedding e preparação para LSTM) e a busca aleatória para otimização dos hiperparâmetros.
- **sarima_sobral.ipynb** e **sarimax_sobral.ipynb**: Implementam modelos SARIMA e SARIMAX para análise de séries temporais.

## Dependências

- Python 3.11.9
- pandas, numpy, matplotlib, seaborn, scikit-learn, TensorFlow/Keras, statsmodels, geopandas, folium

## Como Executar

1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```

2. **Crie e Ative um Ambiente Virtual:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   venv\Scripts\activate     # Windows
   ```

3. **Instale as Dependências:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Execute os Notebooks:**
   ```bash
   jupyter notebook
   ```


## Contato

- **Nome:** Mateus Vasconcelos Albuquerque
- **Email:** mateus.vasconcelos@outlook.com.br

