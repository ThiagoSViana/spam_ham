## Detecta-Spam

Um algoritmo de detecção de Spam usando diferentes modelos de ML, dentre eles: 

- Logistic Regression, 
- Naive Bayes classifier, 
- k-nearest neighbors, 
- Support Vector Machine,
- Random Forest Classifier, 
- Gradient Boosting Classifier,
-  AdaBoost Classifier.

### Requisitos:
Python 3.10

Um ambiente para trabalhar - algo como Jupyter. Se de alguma forma não puder, veja se você pode pelo menos instalar o Python e o pip e, em seguida, use o pip para instalar os pacotes do arquivo requirements.txt.
                 
### Problema:
Mensagens SMS são uma ferramenta muito importante para a comunicação e, para ter uma comunicação eficaz, a filtragem de spam é um dos recursos mais importantes.A detecção de Spam utilizando a abordagem de aprendizado de máquina tem crescido rapidamente, e a redução no custo dos serviços de mensagens resultou no crescimento de anúncios comerciais não solicitados (spams) enviados para telefones celulares. A falta de bancos de dados reais para spams de SMS, mensagens com textos curtos e recursos limitados, além de sua linguagem predominantemente informal são os fatores que podem fazer com que os algoritmos de filtragem de spams estabelecidos tenham um desempenho inferior em sua classificação. Um banco de dados de Spams SMS reais é usado e, após o pré-processamento e extração de recursos, diferentes técnicas de aprendizado de máquina são aplicadas ao banco de dados.

### Descrição do conjunto de dados: 

É utilizado um banco de dados de 1.773 mensagens de texto para treinamento do modelo e, um conjunto de dados de 501 mensagens  para utilizar como dados de teste. O conjunto de dados é um arquivo com diversas linhas, no qual cada linha contém a string da mensagem de texto. Após o pré-processamento dos dados e extração de recursos, técnicas de aprendizado de máquina e outros métodos são aplicados às amostras e seus desempenhos são comparados.

### Pré-processamento de dados, vetor de recursos e modelos usados:
O Dataset tinha duas colunas: 1ª contendo a classe de dados ham ou spam e 2ª contendo uma string que é a mensagem de texto.
As Stopwords em português foram importadas majoritariamente do NLTK, e  algumas outras foram adicionadas manhualmente, todas essas foram removidas se presentes nas frases.
Usamos um vetorizador Count básico da biblioteca Sklearn para tokenizar e vetorizar a string de texto. O Count Vectorizer fornece uma maneira simples de tokenizar uma coleção de documentos de texto e construir um vocabulário de palavras conhecidas, mas também codificar novos documentos usando esse vocabulário. Ele pode ser usado da seguinte forma: a) Crie uma instância da classe CountVectorizer. b) Chame a função fit() para aprender um vocabulário do documento. c) Chame a função transform() no documento conforme necessário para codificar cada um como um vetor. Um vetor codificado é retornado com um comprimento de todo o vocabulário e uma contagem inteira para o número de vezes que cada palavra apareceu no documento.
Obtemos nosso vetor de recursos numérico ou real a partir de uma sequência de mensagens de texto.
Em seguida, foi realizada a divisão em dados de treino e dados de teste na proporção de 70:30, selecionando as amostras aleatoriamente.
Ao fim, os dataset de teste foi utilizado para validar e dar números reais à acurácia do modelo Naive Bayes.
