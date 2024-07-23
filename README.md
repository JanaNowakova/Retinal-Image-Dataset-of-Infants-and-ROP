# Retinal-Image-Dataset-of-Infants-and-ROP
Retinopathy, a term generally used to indicate a retinal involvement, is well-known and well-described, often associated with diabetes mellitus as one of the most concomitant diseases, affecting up to 80% of people with diabetes. Nevertheless, retinopathy connected with diabetes is not the only type of retinopathy. A serious childhood ocular disease is the retinopathy of prematurely born infants - Retinopathy of Prematurity (ROP). As the name suggests, Retinopathy of prematurity (ROP) represents a vasoproliferative disease, especially in newborns and infants, which can potentially affect and damage the vision of premature infants. Despite recent advances in neonatal care and medical guidelines, ROP still remains one of the leading causes of worldwide childhood blindness. 
It is proposed a unique, free-for-non-commercional usage dataset of **6,004 retinal images** of 188 newborns, most of whom are prematurely born infants. **The dataset is accompanied by the anonymized patients' information** from the ROP screening acquired at the University Hospital Ostrava, Czech Republic. Three digital retinal imaging camera systems are used in the study: Clarity RetCam 3, Natus RetCam Envision, and Phoenix ICON.The dataset is prepared for the extension and represents a great basis for developing algorithms to diagnose retinal diseases in children.

To access the whole dataset see **[KAGGLE](https://www.kaggle.com/datasets/e5ffd99802b928a3cbd7b93669599f0697c1842057b2c5641be7ecbb8b7da6a2)** and for more information visit **[https://www.nature.com/articles/s41597-024-03409-7](https://www.nature.com/articles/s41597-024-03409-7)**.

**WHEN USING THE DATASET PLEASE CITE**

Timkovič, J., Nowaková, J., Kubíček, J. et al. **Retinal Image Dataset of Infants and Retinopathy of Prematurity**. Sci Data 11, 814 (2024). https://doi.org/10.1038/s41597-024-03409-7
**https://www.nature.com/articles/s41597-024-03409-7**

Hasal, M., Nowaková, J., Hernández-Sosa, D., Timkovič, J. (2022). Image Enhancement in Retinopathy of Prematurity. In: Barolli, L., Miwa, H. (eds) Advances in Intelligent Networking and Collaborative Systems. INCoS 2022. Lecture Notes in Networks and Systems, vol 527. Springer, Cham. https://doi.org/10.1007/978-3-031-14627-5_43

Hasal, M., Pecha, M., Nowaková, J., Hernández-Sosa, D., Snášel, V., Timkovič, J. (2023). Retinal Vessel Segmentation by U-Net with VGG-16 Backbone on Patched Images with Smooth Blending. In: Barolli, L. (eds) Advances in Intelligent Networking and Collaborative Systems. INCoS 2023. Lecture Notes on Data Engineering and Communications Technologies, vol 182. Springer, Cham. https://doi.org/10.1007/978-3-031-40971-4_44

**BASIC INFORMATION**

The published dataset contains **6,004 images from 188 patients**. Three approaches for image storage are chosen. The set of identical images is stored in three different root folders.  
For the first approach, the root folder (**'images'**) contains folders with the patient's ID (identification), and its subfolders contain identification series. The series represents the same patient, with images taken at varying postconceptual ages (different examination dates). Every subfolder contains the real patient's images taken on the same day from the same patient. Such a division is a user-oriented solution enabling, e.g. educators, quick orientation in the database.
The folder root folder (**'images_stack'**) contains identical images as in the folder 'images', but all images are placed in one folder without other division. 
The third folder (**'images_stack_without_captions'**) is in division similar to (**'images_stack'**), the only difference is, that the images are without any incidental caption/label in the image.
All the images are in the jpg file format. The jpg files were generated with minimal compression when possible with loss-less compression, considering that one of the devices does not allow the png format. All the images are done in the same format with better compatibility with more devices. 
Such a solution is more suitable for machine learning algorithms and data processing.  

The dataset consisted of posterior segment images when part of the poor quality pictures was deleted, but part was left in the dataset (even with worse quality) for dataset variability. There is a big difference between datasets from older people cooperating during the examination. The infant patients are not cooperating, and it is hard to gain only good images.

All images have a name in a predefined format sequentially describing the following values, where the name in brackets is a shortcut for the given parameters, which are divided by an underscore   

**Patient's ID_sex_gestational age (GA)_ birth weight (BW)_ postconceptual age (PA)_ diagnosis code (DG)_ plus-form (PF)_ device(D)_ serie (S)_ image number.jpg.** 

The patient information is also summarized in an Excel file (**infant_retinal_database_info.xlsx**). All information is anonymized and cannot be assigned to a specific patient, even directly by the patient himself.  

For instance, the first patient (001\_F\_GA41\_BW2905\_PA44\_DG2\_PF0\_RC3\_S01\_1) is a female (F) with a gestational age (GA) of 41. week, a birth weight (BW) of 2,905 grams, a postconceptual age (PA) of 44.  week (all the images were taken at this postconceptual age), diagnosis (DG) 2 – hemorrhage, normal (without plus-form), images taken by Clarity RetCam 3, series (S) n. 1. Note that the identification of the given series is present in the name of any file. However, postconceptual age is always the same for given series, and it can handle a distinction between series. 

**INFANT RETINAL DATABASE INFORMATION - PATIENTS' DATA**

| Parameter | Parameter ID | Data type image name | Possible values | Accompanied in image name by |
| --- | --- | --- | --- | --- |
| ID | ID | Integer | - | - | 
| SEX | ID | Category/Char | F/M | - | 
| GESTATIONAL_AGE | GA | Integer | - | GA | 
| BIRTH_WEIGHT | BW | Integer | - | BW | 
| POSTCONCEPTUAL_AGE | PA | Integer | - | PA | 
| DIAGNOSIS_CODE | DG | Category/Integer | - |DG | 
| PLUS_FORM | PF | Integer | - | PF | 
| DEVICE | D | Integer | - | D | 
| SERIES_NUMBER | S | Integer | - | S | 
  
-**Patient's ID, Sex**
The patient's ID (integer) is a unique identifier without any possibility of traceability to a specific patient. The dataset is completely anonymized, and there is no way anybody or even the patient can assign images and data to a specific patient.
The patient's sex is categorical data with a character data type with possible values: Female (F) and Male (M).
The dataset contains images from 188 patients - 94(M) and 94(F). The dataset is balanced in this respect, and there were no used triage parameters. The retinal images according to the sex are in the ratio 3081:2923 for F, resp. M.

-**Gestational age**
The gestational age (integer) is the patient's age at birth in weeks.

-**Birth Weight**
The birth weight (integer) is the patient's weight at birth. 
 
-**Postconceptual Age**
The postconceptual age (integer) is defined as the gestational plus chronological ages (postmenstrual age) in weeks.
The common indicator for the given series of images is the postconceptual age, all images from the series were taken at the same moment. 

-**Diagnosis**
All defined possible diagnoses (categorical data with an integer type) are coded (see List Diagnosis in xlsx table).
There are diagnoses (ROP 4A, 4B and 5) with no images, prepared for further extension.
Two ophthalmological experts did the diagnosis and plus-form ascertaining. The cases where the results differed were discussed with the third expert, and a consensus was reached. Only in approximately 4% of the cases was it necessary to request a third expert opinion.
Note that the diagnosis can change over time, i.e., different series can have varying diagnoses from the same patient (but for most patients, the diagnosis stays the same). The image series of the given patient consists of all images obtained from the examination; the diagnosis can be identifiable from the retinal images in the series. 
Many illnesses are not identifiable only from the images as they have the same or very similar manifestation on the retina, so even the ability to filter healthy and unhealthy patients is valuable.

-**Plus Form**
The plus form is a symptom that can occur in any ROP stage but only in connection with ROP diagnosis, so the number of occurrences is not high. The variable is an integer type with three possible values: 0, 1, or 2. The pre-plus form is not observed in the dataset. The patients' division according to the plus form variable could be confusing as both patients with observed non-normal plus form (PF2) were in the beginning diagnosed as patients with normal plus form (PF0), so these two patients are counted twice - as patients with PF0 and PF2. The definition of pre-plus, and plus form of the disease, is vague, and the patients with pre-plus can be included in the plus-form part. It is also the limitation of all other datasets concerning the pre-plus and plus-form. The incidence of the pre-plus and plus-form is, moreover rare. All the patients with non-normal plus forms were indicated for the treatment.

-**Device**
All series for one patient were done with the same device (categorical with values of the integer type).

-**Series Number**
In one week, more examinations can be done, so the postconceptual age is not unique for examining the patient, and the variable series (integer type) has to be added. Most of the patients (140 patients) were observed moretimes, so there are several series for patients.

