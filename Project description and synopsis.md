![img](https://lh3.googleusercontent.com/hmo7URr9IX51_3VXQlKQlEopMBkA_Df-g5lTOGjXsnQpB8yotihIgNECxODFTTLsKDxHxg63err8KHvdN1z8LcAWpsX9zQ0p3H4VIJVDiyv13-kkB7VSgowzD5KH_hsB_qmNLBG2)

<img src="https://lh4.googleusercontent.com/nDwWCfpOSX80QgdPvgeXu-QMiiVE0VlXHK5NsH49LystlP2UaPnjB1XK8BUaUcYbIHw2NdezsI_9-9FD2CZI045Wd5T8ejrNrEzTCnVeUK412htYJWYSveC7fmjhLcn951DUFZQe" alt="img" style="zoom:80%;" />



# Project description and synopsis

Development of a model of analysis of clinical images for purposes of supporting medical diagnosis 

17 March 2020








# Revisions


<table>
  <tr>
   <td><strong>Version</strong>
   </td>
   <td><strong>Date</strong>
   </td>
   <td><strong>Notes</strong>
   </td>
  </tr>
  <tr>
   <td>1.0
   </td>
   <td>2020-03-17drafting
   </td>
   <td>Document
   </td>
  </tr>
</table>







# Index


[TOC]





# Purpose of the document

This document has the purpose to illustrate the research project that the working group #defeatcovid19 intends to carry out in order to develop a support system for diagnosing lung diseases. The scope of this document will be to present the state of the art in research, in machine learning and to demonstrate the potential of the tool that will be developed including the development path of the research plan.


# State of the art


## Artificial Intelligence (AI) and clinical analysis

Modern clinical imaging techniques are able to offer the doctor valuable information in the early diagnosis of pneumonia with bilateral interstitial infiltrate, typical of serious new coronavirus infections. The use of tools such as radiological analysis during hospitalization and the course of the disease, combined with ultrasound monitoring can provide a clinical picture of the patient, allowing the doctor to take advantage of his experience in order to assess the situation in order to increase the possibility of a favorable prognosis.

The acquisition of images using radiological and ultrasound instruments also allows the doctor to have a scoreboard which, combined with the patient's clinical data, can allow the timely adoption of certain therapy protocols, and monitor their impact over time.

Artificial intelligence in the field of image data processing has produced extremely significant results in recent years. By exploiting the localized nature of the images provided to the machine learning model, it is possible to identify the presence of patterns of interest with a precision that, in the best cases, can go beyond human analysis capacity. Such techniques make extensive use of analytical tools known as neural networks. Such tools (in the generalized mathematical representation) are known as “universal learners”, mathematical models capable of approximating, theoretically, any unknown function. These techniques are effectively applied to classification processes, where the function to be estimated is that of a complex mathematical structure that links the acquired image to the determination of the presence (or absence) of a specific object within it. Neural networks find application in various aspects of the technological frontier: from the simple recognition of the content of an image, to the autonomous driving of vehicles, to the construction of tools capable of "learning" human experience, modeling its behavior. In particular, the latter allow to obtain, through a phase called "training", a machine learning model capable of behaving in front of an image in a similar way to an expert in extracting the information it contains. 

In the medical field, numerous applied research projects have emerged in recent years in which machine learning techniques (or, more generally, artificial intelligence) are used effectively to support the specialist, for the identification and diagnosis of images obtained for the purposes diagnostics from patients, extensively using systems such as computed tomography (CT) [^1] [^2] and Positron Emission Tomography (PET) [^3]. 

Recently, research has focused its efforts on the use of radiological images [^4] and ultrasound [^5] [^6] which, unlike the previous techniques, are extensively adopted to support the diagnosis, not requiring huge financial investments or posing risks for the patient's health.

<p style="font-size:12px">
 1. S. Chen et al., "Automatic Scoring of Multiple Semantic Attributes With Multi-Task Feature Leverage: A Study on Pulmonary Nodules in CT Images," in IEEE Transactions on Medical Imaging, vol. 36, no. 3, pp. 802-814, March 2017. <br/>
 2. Y. Chunran, W. Yuanvuan and G. Yi, "Automatic Detection and Segmentation of Lung Nodule on CT Images," 2018 11th International Congress on Image and Signal Processing, BioMedical Engineering and Informatics (CISP-BMEI), Beijing, China, 2018 , pp. 1-6.<br/>
 3. G. Nalbantov, A. Dekker, D. De Ruysscher, P. Lambin and EN Smirnov, "The Combination of Clinical, Dose-Related and Imaging Features Helps Predict Radiation-Induced Normal-Tissue Toxicity in Lung-cancer Patients - An in -silico Trial Using Machine Learning Techniques, " 2011 10th International Conference on Machine Learning and Applications and Workshops, Honolulu, HI, 2011, pp. 220-224.<br/>
 4. https://www.pyimagesearch.com/2020/03/16/detecting-covid-19-in-x-ray-images-with-keras-tensorflow-and-deep-learning /<br/>
 5. . Liang, R. He, Y. Li and Z. Wang, "Simultaneous segmentation and classification of breast lesions from ultrasound images using Mask R-CNN," 2019 IEEE International Ultrasonics Symposium (IUS), Glasgow, United Kingdom, 2019, pp. 1470-1472.<br/>
 6. L. Zhang, H. Zhu and T. Yang, "Deep Neural Networks for fatty liver ultrasound images classification," 2019 Chinese Control And Decision Conference (CCDC), Nanchang, China, 2019, pp. 4641-4646.<br/>
 </p>






## Screening and diagnosis of patients with COVID19

Following the recent epidemic of new coronavirus, hospitals are under considerable pressure which reaches its peak in the stages of screening for new potentially infected and diagnosis of the course for hospitalized patients, with consequent difficulty for the medical staff in diagnosing both the main situation and any patient's comorbidities. Added to this is the ever increasing need to identify the areas of impact of the virus's action and the course of organs that, although not directly affected, suffer the strong stress induced by the COVID 19 infection. In this scenario, two techniques are present in the diagnostic and monitoring protocols of hospitals: pulmonary radiography and cardiac ultrasound (sometimes also pulmonary). These are techniques aimed at determining the correct physiological functioning of the organs or at assessing the damage in order to be able to reach a prognosis. 


# Synopsis of the studies

This project consists of two complementary studies, with the aim of analyzing the applicability of machine learning models to the analysis of radiological and ultrasound images, in order to build a valid support for medical diagnosis, thus allowing  extending screening procedures to a larger number of patients.

Given the fortunately small number of patients suffering from severe forms of COVID19 and the number usually necessary for the construction of a sufficient dataset to train a new model, we will proceed in this study with the use of previous images available at the hospital representing healthy situations and situations with known pathologies (for example pneumonia) and then the models identified will be specialized by using the available images of COVID19 patients. 

This project aims to conduct two parallel investigations on different types of images and then consolidate the two models identified in a later phase in order to clarify the correlation between cases with similar prognosis. 


## Study 1: Analysis of pulmonary radiological images


### Objectives of the study

A first application of image analysis models regards the radiographs of patients suffering from pneumonia (or suspect cases). By constructing a dataset of images obtained by X-ray and comparing them to the resulting diagnosis, it would be possible to train the model to recognize pathological situations of serious pneumonia. Furthermore, during the course of the disease for hospitalized patients, the use of this analysis model could allow constant monitoring even in conditions of reduced availability of staff, offering feedback to support diagnostic activity.


### Study Population

**Required:** Anonymized lung radiographic image of healthy / pneumonia / COVID19 patients in DICOM format or equivalent. 

**If available,** data of clinical relevance relating to patients such as age, gender, presence of previous pathologies, etc.

**If available** data on COVID19 treatment therapies administered to patients and outcome of the prognosis. 


### Period of study: March 2020 - December 2020


### Analyzed data

The chest and lung x-ray of all available patients will be analyzed, together with the report information, so as to build a dataset useful for training the machine learning model.


### Expected results

A binary classification-model of the probability of favorable or unfavorable diagnosis will be produced, based on the images supplied to the system. The probabilities expressed by the machine learning model can be interpreted as the confidence interval of belonging to one of the two possible diagnosis outcomes.

Expressed outcome and probability will be the two values ​​that can be integrated into the diagnostic evaluation.


## Study 2: Analysis of cardiac (and lung) ultrasound images


### Objectives of the study

The use of ultrasound techniques allows the analysis of the physiological behavior of the organ during examination. In this phase, we will proceed to acquire data produced by an ultrasound machine in use at the hospital for both healthy patients and patients with heart diseases, so as to be able to build a machine learning model capable of identifying pathological behaviors.

The availability of time-varying images relating to the physiology of the cardiac organs of patients will allow training of a machine learning model capable of accurately recognizing a situation of healthy or pathological behavior of the heart muscle.


### Study Population

**Required:** Anonymized images of cardiac ultrasound scans of healthy / pneumonia / COVID19 patients (where available) in DICOM format or equivalent. 

**If available,** data of clinical relevance relating to patients such as age, gender, presence of previous pathologies, etc.

**If** available, data on COVID19 treatment therapies administered to patients and outcome of the prognosis.


### Study period: March 2020 - December 2020


### Analyzed data

The ultrasound images relating to the cardiac function of all available patients will be analyzed, together with the report information, so as to build a dataset useful for training the machine learning model.


### Expected results

A binary classification model of the probability of favorable or unfavorable diagnosis will be produced, based on the images provided to the system. The probabilities expressed by the machine learning model can be interpreted as the confidence interval of belonging to one of the two possible diagnosis outcomes.

Expressed outcome and probability will be the two values ​​that can be integrated into the diagnostic evaluation.





<br>
<br>
<p style="font-size:10px">Neosperience SpA - Share capital: € 726,220.20 iv - Tax code and VAT number: 02792030989 25125
   Brescia, via Orzinuovi, 20 - Tel. +39 030 3537300 - Fax +39 030 3537343
   20129 Milan via Gaspare Gozzi, 1 / A - Tel . +39 02 36755690
</p>
