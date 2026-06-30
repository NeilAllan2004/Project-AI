# Trabalho Final - IA - IFCE Maracanaú

Allan Neil Gomes Pinheiro

Este trabalho apresenta a implementação de quatro problemas utilizando PyTorch e Scikit-Learn:

Questão 1- Inicialmente, foi gerado um conjunto de dados sintético contendo uma variável de entrada e uma variável de saída. Em seguida, aplicou-se a pseudo-inversa para calcular diretamente os parâmetros da reta de regressão (coeficiente angular e intercepto).

Posteriormente, foi implementada uma rede neural equivalente utilizando a biblioteca PyTorch. O modelo foi treinado para minimizar o erro quadrático médio (MSE), permitindo comparar os parâmetros aprendidos pela rede com aqueles obtidos pela solução analítica.

Ao final do treinamento, ambos os modelos foram avaliados utilizando as métricas Mean Squared Error (MSE) e coeficiente de determinação (R²), além da visualização gráfica da reta ajustada aos dados.

Questão 2 - Foi implementado um modelo de regressão logística para resolver um problema de classificação binária utilizando dados sintéticos gerados pela função make_classification da biblioteca Scikit-Learn.

O conjunto de dados foi dividido em treino e teste, sendo utilizado o conjunto de treino para ajustar os parâmetros do modelo e o conjunto de teste para avaliar sua capacidade de generalização. A regressão logística foi implementada como uma rede neural contendo uma única camada linear seguida da função de ativação Sigmoid, responsável por produzir probabilidades entre 0 e 1 para cada classe.

O treinamento foi realizado utilizando gradiente descendente em sua versão não-estocástica, minimizando a função de perda Binary Cross Entropy (BCELoss). Após o treinamento, foi calculada a acurácia no conjunto de teste e gerada a fronteira de decisão do classificador para visualizar a separação entre as classes.

Questão 3 - Foi implementada uma rede neural do tipo Multilayer Perceptron (MLP) para resolver um problema de classificação binária utilizando o conjunto de dados sintético make_moons.

Os dados foram divididos em conjuntos de treino, validação e teste. O conjunto de validação foi utilizado para selecionar automaticamente a melhor arquitetura da rede, evitando que a escolha do número de neurônios fosse baseada apenas no desempenho sobre o conjunto de treinamento.

Foram treinadas quatro arquiteturas diferentes contendo 5, 10, 20 e 50 neurônios na camada oculta. Todas as redes utilizaram função de ativação ReLU na camada intermediária, função Sigmoid na saída, Binary Cross Entropy como função de perda e o algoritmo Adam para otimização dos parâmetros.

Durante o treinamento foi registrada a evolução da função custo ao longo das épocas. Após a comparação das perdas obtidas no conjunto de validação, foi selecionado o modelo com melhor desempenho. Por fim, o modelo escolhido foi avaliado no conjunto de teste e sua fronteira de decisão foi representada graficamente.

Questão 4 - Inicialmente, o conjunto de dados foi carregado utilizando a biblioteca torchvision, que disponibiliza automaticamente as imagens de treinamento e teste. Cada imagem, originalmente no formato 28×28 pixels, foi transformada em um vetor contendo 784 características para ser utilizada como entrada da rede neural.

A arquitetura implementada foi composta por uma camada oculta contendo 64 neurônios com função de ativação ReLU e uma camada de saída contendo 10 neurônios, correspondente às dez classes do problema. O treinamento foi realizado durante 10 épocas utilizando a função de perda CrossEntropyLoss e o otimizador Adam.

Ao término do treinamento, foi calculada a acurácia sobre o conjunto de teste e foram exibidos exemplos de imagens juntamente com as classes previstas pelo modelo, permitindo verificar visualmente o desempenho da rede neural.
