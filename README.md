# Unsupervised-Cross-lingual-alignment-of-Knowledge-BaseTriples-with-Sentences
This project aims to utilise a high resource language ( English) to create an aligned corpus of sentences in a low resource language (Hindi) in a cross-lingual sentting.
We experiment with various static embedding based methods and dynamic contextualised representations using multilingual transformer based models. These lead to strong baselines. We also propose two novel methods for improving on these baselines. We use a gold standard human annotated dataset from multple domains for our evaluation purposes. 
We report significant improvement on evaluating our novel methods on these datasets. This leads to the conclusion that our introduced methods are form an effective basis for cross-lingual alignment task. 
Utilising these alignment models, we create a cross-lingual aligned corpus of English fact triples aligned with Hindi sentences. This corpus, we believe, can be utilised for several downstream tasks like multilingual data-to-text generation, question answering, knowledge base population, knowledge graph completion etc.
We make our code and final aligned corpus publicly available. 

# Aligned Corpus
The aligned dataset is in the follwing json format :
```javascript
{
  "sentence":"",
  "triples":[[]]
  }
Example of a data instance: 
{
  "sentence": "आशीष कक्कड़ ( 21 मई 1971 - 2 नवंबर 2020 ) एक भारतीय फिल्म निर्देशक , लेखक , अभिनेता और आवाज कलाकार थे ।",
  "triples": [["Ashish    Kakkad", "occupation", "film director"], ["Ashish Kakkad", "occupation", "actor"], ["Ashish Kakkad", "occupation", "screenwriter"], ["Ashish Kakkad", "occupation", "artist"], ["Ashish Kakkad", "country of citizenship", "India"]]
  }
```

Our aligned model predictes a set of relevant fact triples for a Hindi sentence. The statistics of the aligned corpus and gold testset are displayed below:

Domain  | Entity Count  |  Sentence Count  | Sentence Count (test data)  | Avg Sentence length (test data) |  Avg Fact Count (test data)|
------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
Actors  | 2106  | 5469  | 50  | 14.32  | 3.60  |
Cricketers  | 2316  | 4694  | 100  | 21.19  | 4.70  |
Politicians  | 3906  | 8916  | 100  | 18.64  | 3.47  |
Writers  | 2755  | 6629  | 50  | 15.65  | 1.78  |
Singers  | 739  | 1944  | 25  | 18.04  | 2.92  |
Journalists  | 607  | 1572  | 25  | 17.32  | 2.12  |
Total  | 12429  | 29224  | 350  | 17.52  | 3.08  |

The link to the aligned corpus and gold standard evaluation dataset is available [here](dataset) 
