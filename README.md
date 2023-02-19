# <i> 'Aariz: </i> A Benchmark Dataset for Automatic Cephalometric Landmark Detection and CVM Stage Classification
<p align="justify">
The accurate identification and precise localization of cephalometric landmarks enable the classification and quantification of anatomical abnormalities. The traditional manual way of marking cephalometric landmarks on lateral cephalograms is monotonous and time-consuming job. Endeavours to develop automated landmark detection systems have persistently been made, however, they are inadequate for orthodontic applications due to unavailability of a reliable dataset. We proposed a new state-of-the-art dataset to facilitate the development of robust AI solutions for quantitative morphometric analysis. The dataset includes 1000 lateral cephalometric radiographs (LCRs) obtained from 7 different radiographic imaging devices with varying resolutions, making it the most diverse and comprehensive cephalometric dataset to date. The clinical experts of our team meticulously annotated each radiograph with 29 cephalometric landmarks, including the most significant soft tissue landmarks ever marked in any publicly available dataset. Additionally, our experts also labelled the cervical vertebral maturation (CVM) stage of the patient in a radiograph, making this dataset the first standard resource for CVM classification. The radiographs from each imaging device are uniformly distributed into train, validation and test sets. We believe that this dataset will be instrumental in the development of reliable automated landmark detection frameworks for use in orthodontics and beyond.

The salient features of our dataset are summarized as follows:
  <ul>
    <li> Our dataset boasts a diverse and extensive collection of <strong> 1000 cephalograms </strong> acquired from <strong> 7 different X-ray imaging devices </strong> with varying resolutions, making it the most comprehensive cephalometric dataset to date. </li>
    <li> The dataset features <strong> 29 most commonly used anatomical landmarks </strong>, with 15 skeletal, 8 dental, and 6 soft-tissue landmarks, annotated by a team of 6 skilled orthodontists in two phases, following extensive labelling and reviewing protocols. </li>
    <li> By annotating the <strong> CVM stages </strong> of each cephalogram in our dataset, we have also created the first standard resource for automatic CVM classification. </li>
  </ul>
</p>

<div align="center">
  <img src="docs/dataset-example-images.svg">
</div>
<div align="center"> A diverse collection of sample images from various imaging devices along with their cephalometric landmarks and CVM stage </div>

# Usage Guide
To create an object of the dataset class and use it to read images and their corresponding annotations, you can first import the <code>AarizDataset</code> and then instantiate the class with the appropriate parameters, such as the <code>dataset_folder_path</code> containing the images and annotations, the <code>mode</code> for which to read the files i.e <code>TRAIN</code>, <code>VALID</code> and <code>TEST</code>.
```
from dataset import AarizDataset
dataset = AarizDataset(dataset_folder_path="folder/to/dataset", mode="TRAIN")
images, landmarks, cvm_stages = dataset[0]
```

# CEPHA29 Challenge 2023
To facilitate the development of robust AI solutions for morphometric analysis, we also organised the <a href="http://vision.seecs.edu.pk/CEPHA29/">CEPHA29 Automatic Cephalometric Landmark Detection Challenge</a> in conjunction with <a href="https://2023.biomedicalimaging.org/en/CHALLENGES.html">IEEE International Symposium on Biomedical Imaging</a> (ISBI 2023). This is a great opportunity for researchers and practitioners in the field to test their algorithms on a standardized platform. We believe that by hosting our dataset as a challenge, we can promote the development of new and innovative solutions to problems in the field.

# Acknowledgements
We would like to express our heartfelt gratitude to all of the clinicians at <a href="https://www.riphah.edu.pk/dental-sciences/">Islamic International Dental College</a> for their tireless efforts and contributions to the annotation process of this dataset. This research would not have been possible without the support of <a href="https://www.riphah.edu.pk">Riphah International University</a>, Islamabad, Pakistan. We also extend our sincere thanks to the patients who provided consent for the use of their cephalometric images. Finally, we would like to acknowledge the valuable feedback and suggestions provided by the anonymous reviewers, which helped us improve the quality of this dataset.

# Cite
Please consider citing our <a href="https://arxiv.org/pdf/2302.07797.pdf">dataset</a> in your research if you find it helpful to your study.
```
@article{
  title={'Aariz: A Benchmark Dataset for Automatic Cephalometric Landmark Detection and CVM Stage Classification},
  author={Khalid, Muhammad Anwaar and Zulfiqar, Kanwal and Bashir, Ulfat and Shaheen, Areeba and Iqbal, Rida and Rizwan, Zarnab and Rizwan, Ghina and Fraz, Muhammad Moazam}
  journal={arXiv preprint arXiv:2302.07797},
  year={2023}
}
```
