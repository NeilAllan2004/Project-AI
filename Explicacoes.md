# Trabalho Final - IA - IFCE Maracanaú

Allan Neil Gomes Pinheiro

Este trabalho apresenta a implementação de quatro problemas utilizando PyTorch e Scikit-Learn:

Questão 1- Inicialmente foi gerado um conjunto de dados sintético composto por uma variável de entrada e uma variável de saída seguindo aproximadamente uma relação linear acrescida de ruído.

Em seguida, foi implementada a solução analítica utilizando Pseudo-inversa, obtendo diretamente os parâmetros da reta de regressão (coeficiente angular e intercepto).

Posteriormente, foi construída uma rede neural simples utilizando PyTorch, composta por uma única camada linear, equivalente matematicamente à regressão linear tradicional. O treinamento foi realizado utilizando o algoritmo Gradient Descent (SGD) com a função de perda Mean Squared Error (MSE).

Ao final do treinamento, foram comparados os parâmetros obtidos pelos dois métodos, bem como as métricas MSE e R², verificando que ambos produziram praticamente os mesmos resultados. Também foi apresentada uma comparação gráfica entre as retas ajustadas.

Questão 2 - Nesta etapa foi implementado um modelo de Regressão Logística para resolver um problema de classificação binária utilizando dados sintéticos gerados pela função make_classification da biblioteca Scikit-Learn.

O conjunto de dados foi dividido em 70% para treinamento e 30% para teste. O modelo foi implementado como uma rede neural composta por uma camada linear seguida da função de ativação Sigmoid, responsável por transformar a saída da rede em probabilidades entre 0 e 1.

O treinamento foi realizado utilizando Gradient Descent (SGD) e a função de perda Binary Cross Entropy (BCELoss).

Após o treinamento, o modelo foi avaliado por meio da acurácia sobre o conjunto de teste e foi construída a fronteira de decisão, permitindo visualizar como a regressão logística separa as duas classes do problema.

Questão 3 - Nesta questão foi implementada uma Rede Neural Multicamadas (MLP) para resolver um problema de classificação binária utilizando o conjunto de dados sintético make_moons, caracterizado por possuir uma separação não linear entre as classes.

Os dados foram divididos em conjuntos de treinamento (70%), validação (15%) e teste (15%).

A arquitetura da rede foi composta por uma camada oculta com ativação ReLU e uma camada de saída contendo um neurônio com ativação Sigmoid. O treinamento foi realizado utilizando a função de perda Binary Cross Entropy (BCELoss) e o otimizador Adam.

Foram treinadas quatro arquiteturas contendo 5, 10, 20 e 50 neurônios na camada oculta. A escolha do melhor modelo foi realizada utilizando o conjunto de validação, selecionando a arquitetura que apresentou a menor Validation Loss.

Ao final, o modelo escolhido foi avaliado sobre o conjunto de teste e sua fronteira de decisão foi representada graficamente, demonstrando a capacidade da MLP de aprender fronteiras não lineares.

Questão 4 - Na última questão foi implementada uma Rede Neural Multicamadas (MLP) para reconhecimento de dígitos manuscritos utilizando o banco de dados MNIST, disponibilizado pela biblioteca torchvision.

O conjunto contém 60.000 imagens para treinamento e 10.000 imagens para teste, sendo cada imagem composta por 28 × 28 pixels. Antes do treinamento, cada imagem foi convertida para um vetor contendo 784 características, correspondente aos seus pixels.

A rede neural foi composta por uma camada oculta contendo 64 neurônios com ativação ReLU e uma camada de saída contendo 10 neurônios, um para cada classe (dígitos de 0 a 9).

O treinamento foi realizado durante 10 épocas, utilizando a função de perda CrossEntropyLoss e o otimizador Adam.

Após o treinamento, o modelo foi avaliado utilizando a acurácia no conjunto de teste. Além disso, foram exibidos exemplos de imagens juntamente com suas respectivas previsões, permitindo verificar visualmente o desempenho do classificador.

Tecnologias utilizadas: PyTorch, Torchvision, NumPy, Matplotlib, Scikit-Learn

Resultados:

1.A solução por Pseudo-inversa e a Rede Neural Linear obtiveram desempenhos praticamente idênticos no problema de regressão.
2.A Regressão Logística foi capaz de separar satisfatoriamente duas classes linearmente separáveis.
3.A MLP apresentou excelente desempenho em problemas de separação não linear, atingindo alta acurácia no conjunto make_moons.
4.A MLP aplicada ao banco MNIST obteve aproximadamente 97,6% de acurácia, mostrando elevada capacidade de reconhecimento de dígitos manuscritos.
