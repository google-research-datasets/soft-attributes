# SoftAttributes: Relative movie attribute dataset for soft attributes

## COPYRIGHT NOTICE

This is the work of Krisztian Balog, Filip Radlinski and Alexandros Karatzoglou from Google LLC, made available under the Creative Commons Attribution 4.0 License. A full copy of the license can be found at https://creativecommons.org/licenses/by/4.0/

## DATA COLLECTION METHODOLOGY

The dataset consists of sets of movie titles, with each set annotated with a single English soft attribute (subjective descriptive property, such as 'confusing' or 'romantic') and a reference movie. For each set, a crowd worker has placed the movies into three sets: more, equally, and less <attribute> than the reference movie. There are 5,991 such sets, from which one can infer approximately 250,000 pairwise preferences over movies for the 60 distinct soft attributes studied.

A full description of the data, methodology, and analyses as well as user instructions can be found in [the associated research paper](https://research.google/pubs/pub50251/), which can be cited as:
```
@inproceedings{balog-et-al-2021-soft-attributes,
  title = {On Interpretation and Measurement of Soft Attributes for Recommendation},
  author = {Krisztian Balog and Filip Radlinski and Alexandros Karatzoglou},
  booktitle = {Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval ({SIGIR})},
  year = 2021
}
```

## EXPLANATION OF DATA FILES

The dataset is provided a CSV format in the file soft-attributes.csv.

Each record consists of a categorization of up to 10 movie titles by a single
rater with regards to a single soft attribute relative to an anchor movie. It
has the following fields:
* rater_id: A unique integer id for each rater from 1 to 100.
* reference_title: The title of the movie with respect to which the ratings are made.
* soft_attribute: The soft attribute with respect to which the ratings are made.
* less_than: List of movie titles judged less <soft_attribute> than <reference_title> 
* about_as: List of movie titles judged about the same <soft_attribute> as <reference_title>
* more_than: List of movie titles judged more <soft_attribute> than <reference_title>

Further details about the data are provided in [Data-Description.pdf](Data-Description.pdf)
