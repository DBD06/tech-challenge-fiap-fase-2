# Tech Challenge FIAP — Fase 2
## Classificação da Qualidade de Vinhos com Machine Learning

### Sobre o projeto

Projeto desenvolvido para o Tech Challenge da Fase 2 da Pós-Tech em Data Analytics da FIAP.

O objetivo é analisar características físico-químicas de vinhos e desenvolver modelos de Machine Learning capazes de identificar vinhos de alta qualidade.

Foi utilizada a base de dados Wine Quality, disponibilizada no Kaggle.

### Objetivos

- Explorar e compreender os dados dos vinhos.
- Investigar correlações entre características químicas e qualidade.
- Realizar o tratamento e a preparação dos dados.
- Treinar e comparar algoritmos de classificação.
- Interpretar os resultados e propor aplicações para o negócio.

### Base de dados

A base original contém 1.143 registros e 11 características físico-químicas.

Para a classificação, foram definidas duas categorias:

- **Classe 0:** vinhos com qualidade inferior a 7.
- **Classe 1:** vinhos com qualidade igual ou superior a 7.

Após a remoção de 125 registros duplicados, foram utilizados 1.018 registros na modelagem.

### Tecnologias utilizadas

- Python
- Google Colab / Jupyter Notebook
- Pandas
- Matplotlib
- Scikit-learn

### Modelos avaliados

Foram realizados três experimentos:

1. Regressão Logística.
2. Árvore de Decisão.
3. Regressão Logística com balanceamento de classes.

### Resultados

| Modelo | Acurácia | Precisão (classe 1) | Recall (classe 1) | F1-score (classe 1) |
|---|---:|---:|---:|---:|
| Regressão Logística | 89,71% | 65% | 48% | 55% |
| Árvore de Decisão | 86,27% | 48% | 37% | 42% |
| Logística Balanceada | 78,43% | 36% | 78% | 49% |

A Regressão Logística original apresentou o melhor F1-score para identificar vinhos de alta qualidade.

A versão balanceada apresentou maior recall, identificando 21 dos 27 vinhos de alta qualidade presentes no conjunto de teste, mas também produziu mais falsos positivos.

### Principais descobertas

O teor alcoólico, os sulfatos e a acidez fixa apresentaram coeficientes positivos relevantes no modelo de Regressão Logística.

A densidade e a acidez volátil apresentaram coeficientes negativos expressivos.

Esses resultados representam associações utilizadas pelo modelo e não demonstram relações de causa e efeito.

### Aplicação ao negócio

Os modelos podem apoiar a triagem inicial de lotes, ajudando a identificar vinhos com maior potencial de qualidade para avaliações adicionais.

A escolha do modelo depende do objetivo da vinícola: encontrar mais vinhos de alta qualidade ou reduzir classificações incorretas.

As previsões não substituem avaliações sensoriais ou análises técnicas complementares.

### Como executar

1. Baixe o notebook `Tech_Challenge_Fase_2_FIAP.ipynb` e o arquivo `WineQT.csv`.
2. Coloque os dois arquivos na mesma pasta.
3. Abra o notebook no Google Colab ou Jupyter.
4. Instale as dependências indicadas em `requirements.txt`, quando necessário.
5. Execute as células na ordem apresentada.

### Estrutura do repositório

- `Tech_Challenge_Fase_2_FIAP.ipynb` — análises, treinamento e avaliação dos modelos.
- `WineQT.csv` — conjunto de dados utilizado.
- `requirements.txt` — bibliotecas necessárias.
- `Apresentacao_Executiva.pdf` — apresentação dos resultados e recomendações.

### Limitações e próximos passos

A base apresenta desbalanceamento entre as classes. Além disso, os modelos foram avaliados em uma única divisão de treinamento e teste.

Como evolução, recomenda-se testar validação cruzada, ajustar hiperparâmetros e avaliar os modelos em novos conjuntos de dados.

## Apresentação em vídeo

O vídeo executivo apresenta o problema de negócio, a análise dos dados, os modelos de Machine Learning, os resultados e as recomendações para a vinícola.

**Assista à apresentação:** https://youtu.be/s-vYetqtEIE

### Autor

Davi Barbosa Domingos

Pós-Tech em Data Analytics — FIAP
