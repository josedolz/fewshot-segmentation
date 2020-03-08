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

### Sample of Weak Annotation (Bounding Box) Generated for FSS-1000 Data set [Download link](https://github.com/rezazad68/fewshot-segmentation/raw/master/FSS-1000%20Bounding%20Box%20Annotation.zip)
![Bounding Box annotation for FSS-1000](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/Weak%20Annotation%20samples%20for%20FSS1000.jpg)


## Results
For evaluating the performance of the proposed method, Two challenging few-shot semantic segmentaion data sets have been considered. In bellow, results of the proposed approach illustrated.
</br>
#### Task 1: FSS-1000: A 1000-Class Dataset for Few-Shot Segmentation
In order to compare the proposed method with state of the art appraoches on  few-shot semantic segmentation, we reported our result using mean Intersection over Unition (mIoU) metric on both 1-shot and 5-shot settings.  

##### Table 1: Results  of  1-way  1-shot segmentation  on  the  FSS-1000 data set  employing  the  mIoU  metric.

Methods | Year |mIoU 
:------------ | :-------------:|:----:
Shaban et. all  [OSLSM](https://arxiv.org/pdf/1709.03410.pdf)        |2017	  |70.29%
Rakelly et. all [co-FCN](https://openreview.net/pdf?id=SkMjFKJwG)        |2018	  |71.94%
Wei et. all     [FSS-1000](https://arxiv.org/pdf/1907.12347.pdf)        |2019	  |73.47%
Hendryx et. all [FOMAML](https://arxiv.org/pdf/1912.06290.pdf)        |2020	  |75.19%
Azad et. all [Proposed Method (Baseline)](https://github.com/rezazad68/fewshot-segmentation)	  |2020 	| 74.19%
Azad et. all [Proposed Method (Baseline + DoG)](https://github.com/rezazad68/fewshot-segmentation)	  |2020 	| 78.71%
Azad et. all [Proposed Method (Baseline + DoG + BConvLSTM)](https://github.com/rezazad68/fewshot-segmentation)	  |2020 	| **80.83%**

##### Table 2: Results  of  1-way  5-shot segmentation  on  the  FSS-1000 data set  employing  the  mIoU  metric.

Methods | Year |mIoU 
:------------ | :-------------:|:----:
Shaban et. all  [OSLSM](https://arxiv.org/pdf/1709.03410.pdf)        |2017	  |73.02%
Rakelly et. all [co-FCN](https://openreview.net/pdf?id=SkMjFKJwG)        |2018	  |74.27%
Wei et. all     [FSS-1000](https://arxiv.org/pdf/1907.12347.pdf)        |2019	  |80.12%
Hendryx et. all [FOMAML+ regularization ](https://arxiv.org/pdf/1912.06290.pdf)        |2020	  |80.60%
Hendryx et. all [FOMAML+ regularization ](https://arxiv.org/pdf/1912.06290.pdf)        |2020	  |82.19%
Azad et. all [Proposed Method (Baseline + DoG + BConvLSTM) non-parametric fusion](https://github.com/rezazad68/fewshot-segmentation)	  |2020 	| 81.65%
Azad et. all [Proposed Method (Baseline + DoG + BConvLSTM) parametric fusion](https://github.com/rezazad68/fewshot-segmentation)	  |2020 	| 83.36%

#### Visual Segmentation result on FSS-1000
Sample of 1-shot segmentation result on the FSS-1000 dataset 
![FSS-1000 Result 1](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/fss1000%20result.jpg)

</br>
#### Task 2: Pascal 5i Dataset for Few-Shot Segmentation
In order to compare the proposed method with state of the art appraoches on  few-shot semantic segmentation, we reported our result using mean Intersection over Unition (mIoU) metric on both 1-shot and 5-shot settings.  

##### Table 1: Results  of  1-way  1-shot & 5-shot segmentation  on  the  Pascal 5i data set  employing  the  mIoU  metric.

Methods | Fold 1 | Fold 2 | Fold 3 | Fold 4| Mean | Fold 1| Fold 2 | Fold 3| Fold 4 | Mean| 1 to 5 shot Improvement
:------------ | :-------------:|:----:| :-------------:|:----:| :-------------:|:----:| :-------------:|:----:|:----:|:----:|:----:
Wei et. all     [FSS-1000](https://arxiv.org/pdf/1907.12347.pdf)|-|-|-|-|-|37.4|60.9|46.6|42.2|56.8|-
Shaban et. all  [OSLSM](https://arxiv.org/pdf/1709.03410.pdf)|33.6|55.3|40.9|33.5|40.8|35.9|58.1|42.7|39.1|43.9|3.1
Rakelly et. all [co-FCN](https://openreview.net/pdf?id=SkMjFKJwG)|36.7|50.6|44.9|32.4|41.1|37.5|50.0|44.1|33.9|41.4|0.3
Rakelly et. all [SG-One](https://arxiv.org/pdf/1810.09091.pdf)|40.2|58.4|48.4|38.4|46.3|41.9|58.6|48.6|39.4|47.1|0.8
Rakelly et. all [AMP](http://openaccess.thecvf.com/content_ICCV_2019/papers/Siam_AMP_Adaptive_Masked_Proxies_for_Few-Shot_Segmentation_ICCV_2019_paper.pdf)|41.9|50.2|46.7|34.7|43.4|41.8|55.5|50.3|39.9|46.9|3.5
Rakelly et. all [PANet](https://arxiv.org/pdf/1908.06391.pdf)|42.3|58.0|51.1|41.2|48.1|51.8|64.6|59.8|46.5|55.7|7.6
Rakelly et. all [Feat Weight](https://arxiv.org/pdf/1909.13140.pdf)|51.3|64.5|56.7|52.2|56.2|54.9|67.4|62.2|55.3|59.9|3.7
Rakelly et. all [Meta-Seg](https://ieeexplore.ieee.org/document/8901116)|42.2|59.6|48.1|44.4|48.6|43.1|62.5|49.9|45.3|50.2|1.6
Rakelly et. all [MDL ](https://ieeexplore.ieee.org/abstract/document/8754235)|39.7|58.3|46.7|36.3|45.3|40.6|58.5|47.7|36.6|45.9|0.6
Rakelly et. all [OSAdv](https://www.sciencedirect.com/science/article/pii/S0020025520300189)|46.9|59.2|49.3|43.4|49.7|47.2|58.8|48.8|47.4|50.6|0.9
Rakelly et. all [AMCG](https://www.aaai.org/ojs/index.php/AAAI/article/view/4860/4733)|-|-|-|-|61.2|-|-|-|-|62.2|1.0
Rakelly et. all [CANet](http://openaccess.thecvf.com/content_CVPR_2019/papers/Zhang_CANet_Class-Agnostic_Segmentation_Networks_With_Iterative_Refinement_and_Attentive_Few-Shot_CVPR_2019_paper.pdf)|52.5|65.9|51.3|51.9|55.4|55.5|67.8|51.9|53.2|57.1|1.7
Rakelly et. all [LTM ](https://arxiv.org/pdf/1910.05886.pdf)|52.8|69.6|53.2|52.3|57.0|57.9|69.9|56.9|57.5|60.6|3.6
Rakelly et. all [PGNet](http://openaccess.thecvf.com/content_ICCV_2019/papers/Zhang_Pyramid_Graph_Networks_With_Connection_Attentions_for_Region-Based_One-Shot_Semantic_ICCV_2019_paper.pdf)|56.0|66.9|50.6|50.4|56.0|57.7|68.7|52.9|54.6|58.5|2.5
Azad et. all [Proposed Method](https://github.com/rezazad68/fewshot-segmentation)|56.2 |66.0 |56.1 |53.8 |58.0|


#### Visual Segmentation result on Pascal 5i
Sample of 1-shot segmentation result on the Pascal 5i dataset 
![Pascal 5i Result 1](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/VOC_segmentation%20result%20.jpg)

### Extra results on FSS1000 data set + Result with Weak Annotation (Bounding Box)
#### Extra Sample of 1-shot segmentation result on FSS1000 data
![FSS1000 Result 2](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/FSS1000%20result%202.jpg)
#### Sample of low-level 1-shot segmentation result on FSS1000 data
![FSS1000 Result 3](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/FSS1000%20bad%20segmentation.jpg)
#### Samples of 1-shot segmentation result on FSS1000 data using weak annotation (bounding box)
![FSS1000 Result 4](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/Weak%20annotation%20result%201.jpg)
![FSS1000 Result 5](https://github.com/rezazad68/fewshot-segmentation/blob/master/githubimages/FSS1000%20bad%20segmentation.jpg)

### Query
All implementation done by Reza Azad. For any query please contact us for more information.

```python
rezazad68@gmail.com

```
