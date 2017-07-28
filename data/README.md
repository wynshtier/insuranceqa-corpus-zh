# InsuranceQA Corpus

This dataset is provided as is and for research purpose only.
If you publish anything using this data, please cite our paper:
Applying Deep Learning to Answer Selection: A Study and An Open Task
Minwei Feng, Bing Xiang, Michael R. Glass, Lidan Wang, Bowen Zhou
ASRU 2015

### Introduction

* This corpus contains questions and answers collected from the website [Insurance Library](http://www.insurancelibrary.com/).
* To our best knowledge, this is the first released QA corpus in the insurance domain
* The content of this corpus consists of questions from real world users, the answers with high quality were composed by professionals with deep domain knowledge. So this is an application with real value, not a toy task.
* In the above paper, the corpus is used for answer selection task. On the other hand, other usage of this corpus is also possible. For example, autonomous learning by reading comprehension of the answers, learning by observation, etc, such that a system can finally come up with its own answer to unseen questions.
* Any ideas to further augment this data set are welcomed. 


### Format
* Latest version is V2, please use the files in the V2 folder. 
* Pool is generated by SOLR.
* File name that includes `raw` contains text with original version.
* File name that includes `token` contains text tokenized with [Stanford Tokenizer](http://nlp.stanford.edu/software/tokenizer.shtml).
* We split the whole corpus into train/valid/test three parts. File name that includes `train/valid/test` corresponds to each part.
* For all tokens starting with `idx_ `, please refer to the vocabulary file for the corresponding word.
* For all train/valid/test files, format is same, with various answer pool size:
 -   ``` <Domain><TAB><QUESTION><TAB><Groundtruth><TAB><Pool>```
* For InsuranceQA.question.anslabel.*:
 -   ```<Domain><TAB><QUESTION><TAB><Groundtruth>```
* For InsuranceQA.label2answer.*
 -  ```<Answer Label><TAB><Answer Text>```
* For vocabulary file:
 -  ```<word index><TAB><original word>```

### Corpus Statistics
|               | Question      |  Answer  | Question Running Words  | 
| ------------- |:-------------:| -----:|   -----:|           
| Train      | 12,889 | 21,325  |    107,889        |
| Valid      | 2,000     |  3354 |   16,931          |
| Test       | 2,000      |    3308 |  16,815            |
There are totally 27,413 answers (answer set size is 27,413) with the 3,065,492 running words of answers.
