# Projeto de Doenças Cardiovasculares - Regressão Logística

## 📌 Sobre o Projeto

O projeto utiliza técnicas de Ciência de Dados e Machine Learning para desenvolver um modelo de classificação capaz de estimar se um paciente apresenta doença cardiovascular a partir de características demográficas, medidas corporais e indicadores relacionados à saúde e aos hábitos de vida.

Foi utilizada a Regressão Logística, um algoritmo de aprendizado supervisionado para classificação binária, com o objetivo de identificar padrões associados à presença ou ausência de doença cardiovascular.

## Problema de Negócio / Pergunta de Pesquisa
É possível utilizar dados históricos de pacientes para desenvolver um modelo de Machine Learning capaz de identificar a presença de doença cardiovascular?

A investigação busca compreender quais variáveis estão associadas à classificação e avaliar a capacidade do modelo de distinguir pacientes com e sem a condição registrada na base de dados.

## 🎯 Objetivo

Construir um modelo que ajude a prever doenças cardiovasculares. O objetivo é utilizar esses dados históricos dos pacientes e construir um bom modelo de regressão capaz de indicar se novos pacientes estão propensos a doenças cardiovasculares ou não.

• Utilização de banco de dados dos pacientes para construir um bom modelo de regressão capaz de indicar se novos pacientes estão propensos a doenças cardiovasculares ou não.

• Construção e avaliação de modelos estatísticos e de machine learning.

• Aplicação de regressão logística, testes de hipóteses e intervalos de confiança.

## 📊 Fonte de Dados

Dataset CARDIO_BASE.csv, com 10.000 registros e 10 colunas, incluindo a variável-alvo cardio_disease.

As variáveis incluem:

- Idade (age) e gênero (gender).
  
- Altura (height) e peso (weight).
  
- Nível de colesterol (cholesterol) e glicose (gluc).
  
- Tabagismo (smoke) e consumo de álcool (alco).
  
- Prática de atividade física (active).
  
- Presença ou ausência de doença cardiovascular (cardio_disease), codificada como 1 ou 0.

O notebook não identifica a instituição ou o endereço original de publicação do dataset; portanto, essa origem não pode ser confirmada a partir do arquivo.

## 🛠️ LINGUAGENS E BIBLIOTECAS

- Python: desenvolvimento do projeto.

- Pandas e NumPy: manipulação e análise dos dados.

- Matplotlib e Seaborn: visualização e análise exploratória.

- Scikit-learn: divisão dos dados, padronização, Regressão Logística, ajuste de hiperparâmetros e avaliação do modelo.

- Imbalanced-learn (SMOTE): balanceamento da base de treinamento.

- GridSearchCV: busca de hiperparâmetros com validação cruzada.

## 🔍 Metodologia

➜ 1. Carregamento e tratamento dos dados
- Leitura do arquivo CSV e inspeção das variáveis.
- Conversão da coluna weight de texto para valores numéricos, com substituição da vírgula decimal e arredondamento para números inteiros.
- Verificação de valores ausentes: nenhum foi identificado.
- Análise estatística descritiva e inspeção das distribuições das variáveis.

➜ 2. Análise exploratória de dados (EDA)
- Análise da distribuição de doença cardiovascular por gênero, prática de atividade física e tabagismo.
- Comparação das médias de idade e peso entre pacientes com e sem a condição registrada.
- Construção de matriz de correlação para investigar relações entre as variáveis.

➜ 3. Preparação dos dados
- Separação das variáveis explicativas (X) e da variável-alvo (Y).
- Divisão dos dados em 80% para treinamento e 20% para teste, utilizando random_state=42.
- Padronização das variáveis com StandardScaler, ajustado somente nos dados de treinamento.
- Aplicação do SMOTE para balancear as classes da base de treinamento, que passou a conter 8.064 registros, distribuídos igualmente entre as duas classes.

➜ 4. Construção do modelo
- Treinamento de um modelo de Regressão Logística.
- Análise dos coeficientes para investigar a contribuição das variáveis na classificação.
- Ajuste de hiperparâmetros com GridSearchCV, validação cruzada de cinco partições e otimização pela acurácia.

➜ 5. Avaliação e simulação de previsões
- Avaliação com matriz de confusão, acurácia, precisão, recall e F1-score.
- Cálculo da curva ROC e da métrica AUC.
- Criação de uma função para simular a previsão de um novo paciente e retornar a probabilidade estimada pelo modelo.

## 📈  Resultados e Métricas


## 💡Principais Insights e Implicações

Principais variáveis associadas à doença cardiovascular

A análise de correlação identificou as seguintes relações positivas com a variável-alvo:

Variável	------ 	Correlação com a variável-alvo

Idade	------ 0,237

Colesterol	------ 	0,221

Peso	------ 	0,183

Glicose	------ 	0,082

Os valores indicam associações lineares positivas, de intensidade relativamente baixa. Isso sugere que essas variáveis, isoladamente, não explicam toda a ocorrência da condição na base analisada.

➜  Insights da análise exploratória

- A idade média foi de aproximadamente 54,9 anos entre os registros com doença cardiovascular, contra 51,7 anos entre os registros sem a condição.

- O peso médio foi de aproximadamente 77,0 kg entre os registros com a condição e 71,6 kg entre os registros sem ela.

- Colesterol e glicose apresentaram correlação positiva de aproximadamente 0,43 entre si.

- Os gráficos de gênero e tabagismo sugeriram diferenças nas contagens entre os grupos, mas essas observações não demonstram, por si só, causalidade ou risco individual.


➜  Implicações para o negócio

- A análise pode ajudar a identificar variáveis que merecem investigação adicional em estudos de saúde.
  
- Modelos de classificação podem apoiar pesquisas sobre estratificação de risco e análise de padrões em dados de pacientes.
  
- O desempenho moderado indica a necessidade de investigar outras variáveis, testar algoritmos alternativos, avaliar diferentes métricas e validar o modelo antes de qualquer aplicação prática.
  
### 𓂃🖊 Apresentação Storytelling: <https://canva.link/87fscfp0uj4oeos>


## 👩‍💻 Sobre a Autora

Desenvolvido por Marina Napoleão — Cientista de Dados / Analista de Dados. 
### LinkedIn <https://www.linkedin.com/in/marina-napoleao/>
### GitHub <https://github.com/marinanapoleao> 
