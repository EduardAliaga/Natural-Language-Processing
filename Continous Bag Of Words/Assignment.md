# Description

In this homework assignment, you will create, analyze, and evaluate word vectors, using a database created from Wikipedia articles.

The baseline notebooks use by default texts from Viquipèdia, the Catalan Wikipedia, but you can create and work with your own Wikipedia database using wikitext to download and preprocess de Wikipedia pages.

# Tasks description

You should use the GPU to train faster! In the settings bar of the notebook -> Accelerators -> GPU. It will ask you to verify first.
## Improve CBOW model
Position-dependent Weighting. The standard CBOW model (CBOW Training notebook) sums all the context word vectors with the same weight. Implement and evaluate a weighted sum of the context words with:
- A fixed scalar weight, e.g, (1,2,2,2,2,1) to give more weight to the words that are closer to the predicted central word
- A trained scalar weight for each position
- A trained vector weight for each position. Each word vector is element-wise multiplied by the corresponding position-dependent weight and then added with the rest of the weighted word vectors.
- (Optional) Hyperparameter optimization: study the performance of the model as a function of one of its parameters: the embedding size, batch size, optimizer, learning rate/scheduler, number of epochs, sharing input/output embeddings.
- (Optional) Implement other methods to obtain word embeddings

## Evaluate the performance of the improved word vectors
- Implement the WordVector class (Word Vector Analysis notebook) with the most_similar and analogy methods to find closest vectors and analogies using the cosine similarity measure.

-  Intrinsic evaluation: perform an informal evaluation finding good and bad examples of closest words and analogies. You can analyze the behavior of the CBOW word vectors for words with multiple meanings, synonyms, and antonyms, word frequency, different types of analogies, bias (gender, race, sexual orientation, etc.).

- (Optional) Visualize word analogies or word clustering properties

- (Optional) Prediction accuracy: compare the accuracy of the implemented CBOW models in the out-of-domain (el Periódico) test set (prediction of the central word given a context of 3 previous and 3 next words). To obtain your score on the competition test set you have to commit your version of the CBOW Training notebook, wait until the training completes, and then "Submit to competition" the obtained file (submission.csv) in the Output section of the notebook.