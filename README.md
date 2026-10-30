# README - Posicionamento Otimizado de Estações de Bicicletas Compartilhadas em Natal/RN com Algoritmo Genético

## 📌 Descrição do Problema

O projeto visa resolver o problema de posicionamento otimizado de estações de bicicletas compartilhadas em Natal/RN. Com base em uma lista de locais candidatos, deseja-se selecionar os melhores pontos para instalar um número fixo de estações de forma a maximizar a cobertura geográfica da cidade.

## 🤖 Metaheurística Utilizada

A metaheurística escolhida foi o **Algoritmo Genético (GA)**, por sua eficácia em resolver problemas de otimização combinatória com múltiplas soluções possíveis. A função de fitness avalia a média das distâncias geográficas entre as estações escolhidas, buscando maximizar a dispersão espacial entre elas.

## 🧩 Variáveis e Restrições

* **Número de estações a serem posicionadas**: 10
* **Candidatos**: lista de locais com latitude e longitude
* **Restrições**: Não repetir locais e escolher apenas locais válidos

## 🛠️ Bibliotecas Necessárias

* pandas
* numpy
* matplotlib
* geopy
* random
* folium


## ▶️ Como Executar o Projeto

1. Faça o upload do arquivo `locais_candidatos.csv` no ambiente do Colab.
2. Execute todas as células do notebook `main.ipynb`.
3. O notebook irá imprimir o melhor conjunto de locais selecionados, gerar um gráfico de convergência e um mapa interativo.

## 📊 Resultados Obtidos

* O GA foi executado com:

  * População: 50 indivíduos
  * Gerações: 100
  * Taxa de crossover: 80%
  * Taxa de mutação: 10%
* O melhor fitness correspondeu à maior média de distância entre as estações, maximizando a área coberta na cidade.
* A solução final incluiu locais estrategicamente distantes, evitando concentração de estações.

### 🌍 Ordem Geográfica dos Locais Selecionados (Norte para Sul)

| Ordem | Nome do Local         | Região         | Observações                                        |
| ----- | --------------------- | -------------- | -------------------------------------------------- |
| 1     | Terminal Zona Norte   | Zona Norte     | Ponto logístico de transporte                      |
| 2     | Mercado da Redinha    | Zona Norte     | Região turística e de comércio                     |
| 3     | Praça Gentil Ferreira | Alecrim/Centro | Região movimentada e histórica                     |
| 4     | IFRN Central          | Centro         | Campus educacional próximo a áreas administrativas |
| 5     | Midway Mall           | Tirol/Centro   | Principal centro comercial                         |
| 6     | Rodoviária            | Lagoa Nova     | Conexão intermunicipal importante                  |
| 7     | Arena das Dunas       | Lagoa Nova     | Ponto turístico e de grande fluxo                  |
| 8     | Shopping Estação      | Zona Sul       | Região com aumento populacional                    |
| 9     | UFRN - Reitoria       | Lagoa Nova     | Campus universitário principal                     |
| 10    | Praia de Ponta Negra  | Zona Sul       | Principal ponto turístico e comercial da cidade    |

### 🗺️ Visualização Geográfica

O notebook gera um mapa interativo com os locais selecionados utilizando a biblioteca **folium**, permitindo uma análise espacial clara da cobertura urbana.

## 💬 Comentários e Conclusões

* O Algoritmo Genético demonstrou boa performance, encontrando soluções diversificadas e espacialmente distribuídas.
* A função de fitness baseada em distância média mostrou-se adequada para o objetivo de cobertura ampla.
* Variações na taxa de mutação e no número de gerações afetam significativamente a qualidade da solução e a convergência.
* Para trabalhos futuros, pode-se incorporar dados de demanda, fluxo urbano ou acessibilidade para refinar a avaliação das localizações.

