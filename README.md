# Semantic-Resume-Matching-Using-Synthetic-Resumes-and-Embedding-Techniques

This project explores automated resume-to-job matching using synthetic resume generation, NLP pipelines, and word embedding techniques. It simulates a real-world recruitment system by aligning job descriptions with generated resumes across three roles: Machine Learning Engineer, Software Engineer, and Database Administrator.

## Key Steps:
Synthetic Data Generation: Created 2,000 resumes using structured templates with randomized experience, tools, degrees, and certifications, based on 2,277 real job descriptions.

# Text Preprocessing: Two spaCy pipelines:

 Basic: Lowercasing, stopword/punctuation removal, tokenization.

 Advanced: Lemmatization, POS tagging, and Named Entity Recognition (NER).

## Embeddings:

spaCy vectors: Averaged en_core_web_lg embeddings.

Word2Vec: Trained with gensim on tokenized data.

BERT: Used bert-base-uncased via HuggingFace Transformers with [CLS] token embeddings.

## Similarity Analysis:
Used cosine similarity to match resumes to job descriptions:

Word2Vec: Strong surface-level similarity (~0.97).

spaCy: Moderate overlap (~0.72–0.93).

BERT: Deep contextual understanding (~0.60–0.84).

## Visualizations:
Applied PCA and t-SNE to visualize embedding alignment:

BERT showed the best semantic clustering between resumes and jobs.

Word2Vec and spaCy had less consistent alignment.

## Outcome:
BERT embeddings provided the most contextually accurate matches, highlighting their strength in real-world resume screening systems. Future enhancements could include incorporating candidate experience length, education level, and multi-sentence encoding for richer comparisons.
