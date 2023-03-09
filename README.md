# Al-Bayan-Quran-QA-Dataset
This repository includes part of the questions dataset we used in "[*Al-Bayan: An Arabic Question Answering System for the Holy Quran*](https://aclanthology.org/W14-3607/)" paper which was published in ANLP workshop co-located with EMNLP 2014.

To use our dataset, please cite our paper using: 

```
@inproceedings{abdelnasser2014bayan,
  title={Al-Bayan: an Arabic question answering system for the Holy Quran}, 
  author={Abdelnasser, Heba and Ragab, Maha and Mohamed, Reham and Mohamed, Alaa and Farouk, Bassant and El-Makky, Nagwa M and Torki, Marwan}, 
  booktitle={Proceedings of the EMNLP 2014 Workshop on Arabic Natural Language Processing (ANLP)}, 
  pages={57--64}, 
  year={2014}
}
```
## Description of Al-Bayan ANER data:

#### The Arabic NER module training data was built using several resources:

1- The labeled Quran in ’[Word by Word - Quranic Arabic Corpus](https://corpus.quran.com/wordbyword.jsp)’. 
This is an annotated linguistic resource which shows the Arabic grammar, syntax and morphology for each word in the Holy Quran. 
The NE tags were obtained by implementing a program that accesses all pages of ’Word by Word’. Then, parsing the html files and extract the NE tags.

2- The numbers in the Quran was labeled using the "الأعداد والنسب في القرآن".

3- The words of the Quran were obtained using [JQuranTree API](https://corpus.quran.com/java/api/index.html). 
JQuranTree: is a set of Java APIs for accessing, analyzing and querying [Tanzil](https://tanzil.net/) XML of Quran in its authentic Arabic form. 
The Java library is released as an open source project.

4- Replacing each pronoun in Quran with its noun using [QurAna](http://textminingthequran.com/).


#### Data format: 
- The training data is in ConNLL2002 format. The data consists of two columns separated by a single space. Each word has been put on a separate line. 
The tags have the same format as in the chunking task: a B denotes the first item of a phrase and an I any non-initial word.

- There are six types of phrases:
```
creation
creator
entity
physical
location
number
```
