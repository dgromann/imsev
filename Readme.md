# Dataset of Inflectional Morpho-Semantic Variants

This repository contains a dataset of morpho-semantic terminological variants of the type of inflectional morphology. The dataset focuses on variants of English plurality for nouns. The plural in each singular-plural word pair is augmented by additional meanings. The dataset was created by filtering WordNet for all plural nouns with additional senses. The following files represent this dataset: 

- plural_variants_without_glosses.txt: word pairs of singular and plura separated by type of inflectional morpheme (marked with ::: at the beginning of the line)

- plural_variants_with_glosses.txt: same as above with all extracted deduplicated senses for the pairs extracted in WordNet 

- plural_variants_manually_removed.txt: all examples that were removed in the manual evaluation process

## Variants with shared meaning vs. Variants without shared meanings

In the process of creating this dataset, two subtypes of plural variants emerged: a) pairs that share meanings, b) pairs that do not share any meanings where the plural may only be used in those plural senses and does not represent a plural of the singular at all. In WordNet each query word is automatically lemmatized, which means each query automatically returns the lemma meanings. Thus, it cannot be used to differentiate between variants with as opposed to variants without shared meanings. We utilized Wiktionary instead and the resulting dataset is provided in the file: FinalAnnotation_usingWiktionary.txt

## Distribution in Vector Space 

As a third experiment, we were interested whether split of shared and no shared meaning is reflected in the distribution of the nearest neighbors in vector space, which we tested with fastText and word2vec pre-trained embeddings. We present the resulting files of pairs where the plural is in the ten nearest neighbors of the singular or not. This separation is presented in the files: nearest_neighbor_evaluation_fasttext.txt and nearest_neighbor_evaluation_word2vec.txt. 

Finally, we upload the similarity results calculated with the cosine distance between the word vectors of the components of each pair in the following two files for the two embedding repositories: sim_results_fastext.txt and sim_results_fastext_word2vec.txt

## Citation
For details and to reference this work please utilize the following information:
Dagmar Gromann and Thierry Declerck (2019): "Towards the Detection and Formal Representation of Semantic Shifts in Inflection Morphology". Proceedings of Language, Data, and Knowledge (LDK)
