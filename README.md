
# References

## NLTK References
* https://www.nltk.org/index.html
* https://realpython.com/nltk-nlp-python/
* https://www.nltk.org/book/ch06.html

## Gensim References
* https://radimrehurek.com/gensim/auto_examples/tutorials/run_doc2vec_lee.html
* https://hekyll.services.adelaide.edu.au/dspace/bitstream/2440/28910/1/hdl_28910.pdf
* https://radimrehurek.com/gensim/auto_examples/core/run_core_concepts.html#core-concepts-corpus
* https://en.wikipedia.org/wiki/Latent_Dirichlet_allocation
* 

# Doc2Vec
Does for full documents what Word2Vec does for words. Achieves better results (in terms of document distinguishability) than e.g. vectorizing all tokens in a text and averaging them or similar document-representation techniques. Probably what we should use.

Plan to train one Doc2Vec model for each approach of:
* every text field is its own document
* every individual's text fields concatenated is a document

## Notes & Caveats
* documents used to train and documents predicted on must be tokenized in the exact same way.
* due to stochastic methods, repeated inferences of the same text will return different vectors
* documents should be most similar to themselves w/ a similarity score of ~1.0, with a meaningful dropoff to the score of the next most similar document
