# NER-with-BERT

### What is BERT?
BERT is basically a trained Transformer Encoder stack, with twelve in the Base version, and twenty-four in the Large version, compared to 6 encoder layers in the original Transformer

BERT encoders have larger feedforward networks (768 and 1024 nodes in Base and Large respectively) and more attention heads (12 and 16 respectively). BERT was trained on Wikipedia and Book Corpus, a dataset containing +10,000 books of different genres

BERT was released to the public, as a new era in NLP. Its open-sourced model code broke several records for difficult language-based tasks. The pre-trained model on massive datasets enables anyone building natural language processing to use this free powerhouse. BERT theoretically allows us to smash multiple benchmarks with minimal task-specific fine-tuning.

 
BERT works similarly to the Transformer encoder stack, by taking a sequence of words as input which keep flowing up the stack from one encoder to the next, while new sequences are coming in. The final output for each sequence is a vector of 728 numbers in Base or 1024 in Large version. (We can use such vectors for our intent classification problem)

### Why do we need BERT?

Proper language representation is key for general-purpose language understanding by machines. Context-free models such as word2vec or GloVe generate a single word embedding representation for each word in the vocabulary. For example, the word “bank” would have the same representation in “bank deposit” and in “riverbank”. Contextual models instead generate a representation of each word that is based on the other words in the sentence. BERT, as a contextual model, captures these relationships in a bidirectional way. (BERT was built upon recent work and clever ideas in pre-training contextual representations including Semi-supervised Sequence Learning, Generative Pre-Training, ELMo, the OpenAI Transformer, ULMFit and the Transformer. Although these models are all unidirectional or shallowly bidirectional, BERT is fully bidirectional.)

### About NER

Named Entity Recognition (NER) is a usual NLP task, the purpose of NER is to tag words in a sentences based on some predefined tags, in order to extract some important info of the sentence.
Here is an example:
E.g.
Sentence: “Taylor Swift will launch her new album in Apple Music.”
NER result:“Taylor[B-PER] Swift[I-PER] will[O] launch[O] her[O] new[O] album[O] in[O] Apple[B-ORG] Music[I-ORG].[O]”

In NER, each token in the sentence will get tagged with a label, the label will tell the specific meaning of the token.
So that, through NER, we can analyze the sentence with more details and extract some important info.

### Data Description
(https://www.kaggle.com/abhinavwalia95/entity-annotated-corpus?select=ner_dataset.csv)


