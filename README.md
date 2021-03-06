# <h1 align="center">Word Similarity Visualization</h1>
### An example of <b>word similarity visualization</b> using an Word2Vec model and networkx

## Libs and tools:

- [Python](https://www.python.org/): version 3.7.5
- [Pandas](https://pandas.pydata.org/): version 1.1.1
- [Numpy](https://numpy.org/): version 1.17.3
- [NLTK](https://www.nltk.org/): version 3.5
- [Gensim](https://radimrehurek.com/gensim/): version 3.8.0
- [Scikit-learn](https://scikit-learn.org/stable/): version 0.23.2
- [Plotly](https://plotly.com/): version 4.14.1
- [Networkx](https://networkx.org/): version 2.5
- [Yellowbrick](https://www.scikit-yb.org/en/latest/index.html): version 1.3


---
<h1 align="center">Project Description</h1>

<p>This repository provides an example of word similarity visualization. Here we use a word2vec model that vectorizes each word, cosine similarity to calculate the distance between each word vector and networkx to plot the word embedding into a graph structure</p>

<p>The example uses a news dataset and the model is trained using the headlines of three different categories: Politics, Entertainment and Travel</p>

<p>The model generates vector to represent each word. So, we can apply a lot of methods in the vectors space, like cosine similarity, to obtain the most similar words. This can be use to form clusters of words</p>

![alt text](https://github.com/AlexandreH13/word_similarity_visualization/blob/main/imgs/word2vec.png?raw=true)


---
<h1 align="center">Results</h1>

<p><h2>Clustering</h2></p>
<p>First we use the word vectors in a Kmeans method to see how well the groups(news categories) are splitted. To determine the optimal numbers of clusters, the elbow method was applied. We can see in the image below that the optimal number of clusters matches with the number of categories.</p>

![alt text](https://github.com/AlexandreH13/word_similarity_visualization/blob/main/imgs/elbow_method.png?raw=true)

<p>To see if the groups were formed correctly, we provide words from each category and check if its groups are the same.</p>

![alt text](https://github.com/AlexandreH13/word_similarity_visualization/blob/main/imgs/w_groups.png?raw=true)

<p><h2>Visualization</h2></p>
<p>Finally, we plot the clusters using the graph structure. As can be seen in the image below, a graph is created were its vertices represents the words in the vocabulary and the edges represents the distance (similarity)</p>

![alt text](https://github.com/AlexandreH13/word_similarity_visualization/blob/main/imgs/newplot.png?raw=true)