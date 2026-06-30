<h1>📘 Transformação e preparação de dados </h1>
<p align="justify">
O armazenamento de grande volume de dados se tornou necessário em relação a diversidade e variedade de fontes de coletas de informações. Atualmente, temops acesso a uma gama de base de dados, porém, é importante como trabalhamos com esses dados.
</p>

<h2>💡 Extract, transform, Load - ETL</h2>
<p align="justify">
É um tipo de data integration em três etapas, extração, transformação e carregamento. Usado para combinar dados de diversas fontes. Nesse processo, os dados são extraidos de um sistema fonte, convertidos em um formato que possa ser analisado e armazenados. 
</p>

<h2>💡 Descritores visuais</h2>
<p align="justify">
Um descritor visual de uma face, descreve principais caracteristicas de uma face relacionadas a informação de textura, cor e brilho. 
</p>

#### Leitura de imagem em Python

```
# Importar bibliotecas
import cv2
import numpy as np
from IPython.display import Image
import matplotlib.pyplot as plt
import matplotlib

# Leitura da imagem
img = cv2.imread('imagem.png')

# Apresentação da imagem na tela
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.show()
```

#### Detecção de face em Python
```
#Dimensão das imagens
plt.rcParams['figure.figsize'] = (224, 224)

#Classificador construído para detectar faces
face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')

#Transformando a imagem em escala de cinza
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

#Processo para detectar as faces na imagem
faces = face_cascade.detectMultiScale(
 gray,
 scaleFactor=1.1,
 minNeighbors=5,
 minSize=(30, 30),
)

cont = 0
for (x,y,w,h) in faces:
 img = cv2.rectangle(img,(x,y),(x+w,y+h),(255,0,0),2)
 roi_gray = gray[y:y+h, x:x+w]
 roi_color = img[y:y+h, x:x+w]
 cont=cont + 1

cv2.imwrite('aragorn.png',img)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.show()
```

#### Construção de um gráfico de cores em Python
```
#Dimensão das imagens
plt.rcParams['figure.figsize'] = (224, 224)

#Classificador construído para detectar faces
face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')

#Transformando a imagem em escala de cinza
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

#Processo para detectar as faces na imagem
faces = face_cascade.detectMultiScale(
 gray,
 scaleFactor=1.1,
 minNeighbors=5,
 minSize=(30, 30),
)

cont = 0
for (x,y,w,h) in faces:
 img = cv2.rectangle(img,(x,y),(x+w,y+h),(255,0,0),2)
 roi_gray = gray[y:y+h, x:x+w]
 roi_color = img[y:y+h, x:x+w]
 cont=cont + 1

cv2.imwrite('aragorn.png',img)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.show()
```

### Descritor de textura
<p align="justify">
Descrevem caracteristicas de distribuição espacila e variação de luminosidade, fornecendo, também, informação sobre o arranjo estrutural das superficies. Divididas em três abordagens:
</p>
<p align="justify">
<b>Abordagem estatistica:</b> São metodos que não se preocupam em representar a estrutura hierarquica das texturas, mas buscam representar de forma indireta por meio de metodos não deterministicos, com uma analise das vizinhanças dos pixels entre niveis de cinza. Essa abordagem analisa os vizinhos de cada pixel e tenta estabelecer um padrao por meio dos tons de cinza. 
</p>
<p align="justify">
<b>Abordagem baseada em modelos parametricos:</b> Definidos por um modelo composto por um conjunto de parametros extraidos de forma não deterministica.
</p>
<p align="justify">
<b>Abordagem baseada em processamento de sinais:</b> Por meio de transformações de uma imagem, são extraidos descritores de textura, sendo essa abordagem escolhida por esse trabalho para compor a assinatura visual das faces.
</p>

### Descritor de cor
<p align="justify">
O espaço espectral de luz visivel possui dimensão infinita. Para realizar a representação de uma cor, é necessário "descretizar" esse espaço e obter uma representação de diemensão finita capaz de ser reconstruida e estar percentualmente proxima a cor. 
</p>
<p align="justify">
Os descritores de cor podem ser obtidos por meio do calculo do histograma, que consiste no caclculo estatistico dado pela distribuição de frequencias de uma massa de medições.
</p>

### Bag of Words
<p align="justify">
A modelagem Bag Of Words utiliza uma presentação espacial de documentos textuais. Cada documento é rpesentado por um vetor de n dimensões, em que n é o numero de termos na coleção de documentos. O objetivo dessa técnica é representar um conjunto de palavras por meio de um vetor dimensional e capturaras frequencias de ocorrencia de palavras no corpo do texto.
</p>
<p align="justify">
Também é utilizada como recurso em tarefas como analise de sentimentoe identificação de topicos em documentos textuais: Analise de sentimento, tradução de texto, extração de relaçaõ de documentos, maquinas de busca e chatbots.
</p>
<p align="justify">
O modelo é uma ferramenta cujo objetivo é extrair e processar informações que possuem natureza textual com o intuito de auxiliar o processo de modelagem de dados que antecipam a utilização de tecnicas de algoritmos de aprendizado de maquina. Esse processo envolve tres etapas: <br>
1: Identificar vocabulario das palavras presentes nos documentos;<br>
2: Excluir os termos que não são necessarios (stopwords);<br>
3: Contabilizar a frequencia de cada termo para todos os documentos da colecao;<br>
 abordagem possuis problemas ao contabilizar apenas a frequencia das palavras presentes nos documentos. Palavras que possuem uma alta frequencia nos documentos impactam a representação dos documentos e esses termos não podem não conter um conteudo relevante para o modelo quando comparados aos termos menos frequentes. Para amenizar, é realizado o redimensionamento da frequencia das palavras de acordo com a periodicidade que aparecem em otdos os documentos, essa abordagem é chamada de TF-IDF (frequency-inverse documento frequency), que é uma medida estatistica, com objetivo de indicar a importancia de uma palavra em um docuimento em relação a uma coleção de documentos.
</p>

####  Bag of Words em Python
```
from sklearn.feature_extraction.text import CountVectorizer

corpus = [
     'This is the first document.',
     'This document is the second document.',
     'And this is the third one.',
     'Is this the first document?',
]
vectorizer = CountVectorizer()
X = vectorizer.fit_transform(corpus)
print(vectorizer.get_feature_names())

Resultado:

['and', 'document', 'first', 'is', 'one', 'second', 'the', 'third', 'this']

print(X.toarray())
Resultado:

[[0 1 1 1 0 0 1 0 1]
 [0 2 0 1 0 1 1 0 1]
 [1 0 0 1 1 0 1 1 1]
 [0 1 1 1 0 0 1 0 1]]
 ```

 <h2>Tecnicas Avançadas</h2>
 <p align="justify">
Técnicas de aprendizagem de máquina que podem ser aplicadas para a preparação de dados. Em muitos casos, os dados podem não estar rotulados, e técnicas de agrupamento e/ou classificação podem ser empregadas para amenizar essa situação.     
</p>

### Agrupamento
 <p align="justify">
Clustering, como também é conhecido, é o nome dado ao grupo de técnicas computacionais cujo propóstio consiste em separar objetos em grupos, com base nas caracteristicas que esses objetos possuem. Essa técnica é usada em diversas areas de pesquisa:<br>
<b>Documentos:</b>agrupamento de documentos de acordo com similaridade semantica.<br>
<b>Imagem:</b> agrupamento de imagens por meio da similaridade de seu conteudo visual.<br>
<b>Perfil:</b> analise do perfil de clientes de cartão de credito<br>
</p>

### Heuristicas de agrupamento: K-Means
 <p align="justify">
É uma heuristica de agrupamento que busca minimizar a distancia dos elementos em relação ao conjunto de K centro. Passo a passo para agrupar itens com essa técnica:<br>
1: Escolher k de distintos valores para centro de grupo;<br>
2: Associar cada ponto ao centro mais proximo<br>
3: Recalcular o centro de cada grupo;<br>
4: Repetir passos 2 e 3 até nenhum elemento mudar de grupo  

```
Eis um exemplo em Python que utiliza K-Means para agrupar itens: 

from sklearn.cluster import KMeans

import numpy as np

X = np.array([[1, 2], [1, 4], [1, 0],[4, 2], [4, 4], [4, 0]])

kmeans = KMeans(n_clusters=2, random_state=0).fit(X)

print kmeans.labels_

kmeans.predict([[0, 0], [4, 4]])

print kmeans.cluster_centers_
```
</p>

<h2>Métodos e técnicas de organização e visualização de dados</h2>
<p align="justify">
A qualidade de dados é de suma importancia, tanto na coleta quanto na preparação. A analise de dados tem que estar alinahda com a visão e estrategia de negocio, de tecnologia de informação da empresa de modo que os resultados sejam direcionados para uma tomada de decisão. Para que os resultados da analise de dados sejam documentadas e apresentadas, fazemos o uso de metodos e técnicas de organização e visualização de dados, dashboard e ferramentas de visualização de dados.     
</p>

#### Visualização de dados
<p align="justify">
A visualização de dados permite repreentar visualmente as informações cuja forma agregada resumo e contextualiza melhor os dados: infograficos, visualização cientifica e gráficos estatisticos. Relatorios empresariais podem ser apresentados na forma de relatorios de métricas de gestao cujo desempenho é administrado por meio de metricas orientadas para resultados (KPIs). <br>
Ou dashboards, cujo apresentação é grafica com varios indicadores de desempenho em uma unica página com indicadores. <br>
O relatrio balanced scorecard, apresenta um plano informações de clientes, processos comerciais, aprendizado e crescimento.
</p>