English Description Below

Projeto: 

Classificação de Dígitos com Ensemble Learning

Sobre o Projeto

Neste projeto, utilizei o dataset MNIST 784, que contém imagens de dígitos manuscritos, 
para aplicar diferentes técnicas de ensemble learning e avaliar seu desempenho em tarefas de classificação. 

O foco está em três abordagens principais:

Stacking Ensemble Manual

Voting Classifier

StackingClassifier do scikit-learn

A partir dessas técnicas, analisei como diferentes modelos combinados podem melhorar a acurácia final na predição dos dígitos.

Passos Seguidos

1. Carregamento dos Dados

Utilizei o dataset MNIST 784 disponível no OpenML, que contém 70.000 imagens de dígitos manuscritos (28x28 pixels).
Separei os dados em conjuntos de treino (80%) e teste (20%) para avaliação.

2. Pré-processamento

Escalei os dados utilizando o StandardScaler para padronizar as features e melhorar o desempenho dos modelos.

3. Treinamento de Modelos Individuais

Treinei os seguintes modelos base:

Logistic Regression (LR)

Random Forest (RF)

Support Vector Classifier (SVC)

4. Criação do Ensemble Manual (Stacking)

Realizei uma abordagem manual para criar um modelo de Stacking Ensemble:

Utilizei predições cruzadas (cross_val_predict) dos modelos base no conjunto de treino para gerar uma nova matriz de dados.

Treinei um modelo de Logistic Regression como "blender" para combinar as predições dos modelos base.

No conjunto de teste, combinei as predições dos modelos base para fazer as predições finais usando o "blender".

5. Voting Classifier

Implementei um Voting Classifier, que combina os modelos base com uma abordagem de votação majoritária (hard voting) para comparar com os outros modelos.

6. StackingClassifier do scikit-learn

Usei a implementação do StackingClassifier do scikit-learn para comparar seu desempenho com o método manual.

7. Avaliação dos Modelos

Calculei a acurácia final de cada abordagem nos dados de teste:

Ensemble Manual (Stacking): 94,78%

Voting Classifier: 96,71%

StackingClassifier: 97,65%





Digit Classification with Ensemble Learning

About the Project

In this project, I used the MNIST 784 dataset, which contains images of handwritten digits, 
to apply various ensemble learning techniques and evaluate their performance on classification tasks.

The focus is on three main approaches:

Manual Stacking Ensemble

Voting Classifier

StackingClassifier from scikit-learn

Using these techniques, I analyzed how combining different models can improve the final accuracy in digit prediction.

Steps Followed

1. Data Loading

I utilized the MNIST 784 dataset from OpenML, which includes 70,000 images of handwritten digits (28x28 pixels).
The dataset was split into training (80%) and testing (20%) sets for evaluation.

2. Preprocessing

Data was scaled using StandardScaler to standardize the features and enhance model performance.

3. Training Individual Models

The following base models were trained:

Logistic Regression (LR)

Random Forest (RF)

Support Vector Classifier (SVC)

4. Manual Stacking Ensemble

I created a manual Stacking Ensemble model with the following steps:

Used cross_val_predict to generate predictions from the base models on the training set, creating a new feature matrix.
Trained a Logistic Regression model as a "blender" to combine the base models' predictions.

On the test set, combined predictions from the base models and made final predictions using the "blender."

5. Voting Classifier

Implemented a Voting Classifier, which aggregates predictions from the base models using majority voting (hard voting) to compare with other ensemble methods.

6. StackingClassifier from scikit-learn

I used the StackingClassifier from scikit-learn for comparison with the manual stacking method.

7. Model Evaluation

The final accuracy of each approach on the test set was as follows:

Manual Stacking Ensemble: 94.78%

Voting Classifier: 96.71%

StackingClassifier: 97.65%
