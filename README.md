# fewshot-segmentation

# [On the Texture Bias for Few-Shot CNN Segmentation]()

This repository contains the code for deep auto-encoder-decoder network for few-shot semantic segmentation with state of the art results on FSS 1000 class dataset and Pascal 5i. This method embeds different ferequncy information in the CNN representation to overcome with the texture bias and applies bidirectional convolutional LSTM layers to perform non-liner parametric k shot setting for few-shot semantic segmentation. If this code helps with your research please consider citing the following paper:
</br>
> [R. Azad](https://scholar.google.com/citations?hl=en&user=Qb5ildMAAAAJ&view_op=list_works&sortby=pubdate),
[Abdur. R. Fayjie](https://sites.google.com/site/abdurrfayjie/),
[Ismail Ben Ayed](https://scholar.google.com/citations?hl=en&user=29vyUccAAAAJ&view_op=list_works&sortby=pubdate),
[Marco Pedersoli](https://scholar.google.com/citations?user=aVfyPAoAAAAJ&hl=en) and
[Jose Dolz](https://scholar.google.ca/citations?user=yHQIFFMAAAAJ&hl=en) 
"On the Texture Bias for Few-Shot CNN Segmentation", arXiv preprint arXiv, 2020, download [link]().

#### Please consider starring us, if you found it useful. Thanks

## Updates
will be update soon


## Prerequisties and Run
This code has been implemented in python language using Keras libarary with tensorflow backend and tested in ubuntu OS, though should be compatible with related environment. following Environement and Library needed to run the code:

- Python 3
- Keras version 2.2.0
- tensorflow backend version 1.13.1


## Run Demo
For training deep model ....










## Quick Overview
![Diagram of the proposed method](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/Figure1.png)

### Structure of the Proposed Scale Space encoder for reducing texture bias effect
![Diagram of the SSR](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/Figure2.png)

## Results
For evaluating the performance of the proposed method, Two challenging few-shot semantic segmentaion data sets have been considered. In bellow, results of the proposed approach illustrated.
</br>
#### Task 1: FSS-1000: A 1000-Class Dataset for Few-Shot Segmentation
In order to compare the proposed method with state of the art appraoches on  few-shot semantic segmentation, we reported our result using mean Intersection over Unition (mIoU) metric on both 1-shot and 5-shot settings.  

Table 1: Performance comparision 

Methods | Year |mIoU 
:------------ | :-------------:|:----:
Shaban et. all  [OSLSM](https://arxiv.org/pdf/1709.03410.pdf)        |2017	  |70.29%
Rakelly et. all [co-FCN](https://openreview.net/pdf?id=SkMjFKJwG)        |2018	  |71.94%
Wei et. all     [FSS-1000](https://arxiv.org/pdf/1907.12347.pdf)        |2019	  |73.47%
Hendryx et. all [FOMAML](https://arxiv.org/pdf/1912.06290.pdf)        |2020	  |75.19%
Azad et. all [Proposed Method (Baseline)](https://github.com/rezazad68/fewshot-segmentation)	  |2020 	| 74.19%
Azad et. all [Proposed Method (Baseline + DoG)](https://github.com/rezazad68/fewshot-segmentation)	  |2020 	| 78.71%
Azad et. all [Proposed Method (Baseline + DoG + BConvLSTM)](https://github.com/rezazad68/fewshot-segmentation)	  |2020 	| **80.83%**


#### Visual Segmentation result on FSS-1000
Sample of 1-shot segmentation result on the FSS-1000 dataset 
![FSS-1000 Result 1](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/fss1000%20result.jpg)


### Acknowledgement 
We warmly thanks Chez Alexandra group for supporting our research study while performing this research

### Query
All implementation done by Reza Azad. For any query please contact us for more information.

```python
rezazad68@gmail.com

```
