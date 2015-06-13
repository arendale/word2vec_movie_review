# word2vec_movie_review
## Bag_of_Words_model
This is an ensemble of code sections in tutorial. Please refer to tutorial Part 1.

## Word2Vec
This is copied from tutorial Part 2. It is worth pointing out that `Logistic Regression` works better than `Random Forest`.

## Doc2Vec
Both `Bag of Words` and `Word2Vec` lose word order information in review. To solve this problem, `Doc2Vec` vectorizes sentences
in review and generate averaged sentence vectors for each review. The aggregation of averaged word vector and sentence vector 
represents document, A.K.A. review.

## TFIDF_Word2Vec
Same as `Word2Vec` except word vectors are weighted according to TFIDF score when we average word vectors.

## TFIDF_Word2Vec_Doc2Vec
Same as `Doc2Vec` except word vectors are weighted according to TFIDF score when we average word vectors.

## CRP_Word2Vec
Chinese Restaurant Process is implemented to cluster words by calculating distance (cosine similarity) from `movie`, 
`film` and `review`. The farthest clusters are removed to reduce noise in review.

## CRP_Word2Vec_TFIDF
Same as `CRP_Word2Vec` except word vectors are weighted according to TFIDF score when we average word vectors.

## Phrase2Vec
To partial keep the order of words, phrases above certain frequency threshold like `los angeles`, `a bit of` are vectorized instead
of single word. The rest part is same as `Word2Vec`.

## Phrase2Vec_TFIDF
Same as `Phrase2Vec` except word vectors are weighted according to TFIDF score when we average word vectors.

## ShallowLearning
Someone posted this code in forum that beats all `Word2Vec` models. The name is for making fun of `Deep Learning`. The idea is to
use TFIDF score of each word in one review as vector representing the review. It is simple and very accurate. 
