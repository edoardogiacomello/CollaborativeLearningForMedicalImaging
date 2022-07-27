# Addressing Collaborative Machine Learning Challenges in Medical Imaging
Codebase for my Ph.D. thesis: "[Addressing collaborative machine learning challenges in medical imaging](http://hdl.handle.net/10589/188696)"

## Abstract
<details>
  <summary>
   Collaborative Machine Learning is a vast area of research that includes a set of techniques, such as Distributed Learning and Esembling Methods, to enable multi-centric studies using multiple private datasets. The main idea behind collaborative machine learning is to share knowledge instead of data to overcome potential privacy issues in exchanging sensitive data. [Click Here for Full Text]
  </summary>
  Machine Learning and Deep Learning tools in Medical Imaging are promising approaches to aid physicians and radiologists in performing diagnoses. Machine Learning models that work with imaging data require massive amounts of data. Although many institutes are collaborating to produce publicly available datasets of medical images, the process of data acquisition is severely limited by different challenges. These challenges are mainly related to privacy regulations and the effort of domain experts to assess imaging data quality and produce high-quality ground truth. In turn, the difficulty of managing large datasets of medical imaging translates in a scarcity of data available for research. This Ph.D. thesis studies collaborative machine learning as a methodological approach to overcome the problem of data availability. Collaborative Machine Learning is a vast area of research that includes a set of techniques, such as Distributed Learning and Esembling Methods, to enable multi-centric studies using multiple private datasets. The main idea behind collaborative machine learning is to share knowledge instead of data to overcome potential privacy issues in exchanging sensitive data. However, this approach poses challenges that include data heterogeneity due to the population included in the datasets, and data incompleteness, due to different data acquisition standards and practices among different institutions. This work provides a general taxonomy for classifying the various approaches proposed in the literature. We analyze well-established techniques such as ensemble learning and transfer learning in the context of collaborative machine learning. Moreover, we analyze more recent contributions based on distributed learning, comparing their performances according to data heterogeneity and privacy constraints. Our experiments study multiple approaches that exploit ensemble methods, distributed learning, and transfer learning to overcome different challenges, such as data heterogeneity, model heterogeneity, and label heterogeneity using public and private datasets. Finally, we propose our approach to image segmentation based on adversarial networks and generative adversarial networks to study possible approaches to the problem of incomplete medical imaging datasets. The results are promising, showing that collaborative learning can successfully overcome the issues above. In particular, ensemble learning methods can build a single model from multiple models with different architectures when trained on different data subsets. Moreover, distributed learning approaches proved to be a good design choice when privacy has to be attained, especially in a context of data heterogeneity. Transfer learning and embedding techniques can enable the training of custom models on smaller private datasets by exploiting the powerful feature extraction modules of Convolutional Neural Networks. Lastly, our approach based on adversarial networks proved to be promising to enable the use of multi-input segmentation models when some of them are missing, thanks to image translation.
</details>


## Setup
This codebase is meant to be run on Docker Images. See [JupyterHubGPU](https://github.com/edoardogiacomello/JupyterHubGPU) for a collaborative environment or [here](https://github.com/edoardogiacomello/ProjectsEnvironment) for a local docker image.

### WARNING
While the majority of experiments are made with Tensorflow 2.0, some of them requires the version 2.0a. Due to a bug in BatchNorm layer, models trained with 2.0a and 2.0 (stable) are NOT COMPATIBLE (they would output a wrong result). As a rule of thumb, all models trained on BraTS 2015 require TF 2.0a, while all the others require TF 2.0.


## CodeBase

This project is made of multiple independent sub-modules. 

### Chapter 4.1: Ensembling Methods for Image Segmentation 

See [DistributedSegmentation](https://github.com/edoardogiacomello/DistributedSegmentation) submodule.

### Chapter 4.2: Ensembles of Heterogeneous Models 

See [ChestXRayEnsembling](https://github.com/edoardogiacomello/ChestXRayEnsembling) submodule.


**Article**<details>
  <summary> 
  Image embedding and model ensembling for automated chest x-ray interpretation.
  </summary>
  Edoardo Giacomello, Pier Luca Lanzi, Daniele Loiacono, and Luca Nassano. Image embedding and model ensembling for automated chest x-ray interpretation. 2021 International Joint Conference on Neural Networks (IJCNN), 2021.
</details>

### Chapter 5: Distributed Learning - Comparison of Federated Learning and Split Learning for
Healthcare Imaging 

See [FederatedLearningVsSplitLearningHealthcare](https://github.com/edoardogiacomello/FederatedLearningVsSplitLearningHealthcare) submodule.



**Article**<details>
  <summary> 
  Distributed learning approaches for automated chest x-ray diagnosis.
  </summary>
  Edoardo Giacomello, Michele Cataldo, Daniele Loiacono, and Pier Luca Lanzi. Distributed
learning approaches for automated chest x-ray diagnosis. arXiv preprint arXiv:2110.01474,
2021.
</details>

### Chapter 6.1: Model Training using Image Embeddings 

See [ChestXRayEnsembling](https://github.com/edoardogiacomello/ChestXRayEnsembling) submodule.

**Article**<details>
  <summary> 
  Image embedding and model ensembling for automated chest x-ray interpretation.
  </summary>
  Edoardo Giacomello, Pier Luca Lanzi, Daniele Loiacono, and Luca Nassano. Image embedding and model ensembling for automated chest x-ray interpretation. 2021 International Joint Conference on Neural Networks (IJCNN), 2021.
</details>

### 6.2 Transfer Learning using Embeddings on a Private Dataset 

Codebase not publicly available. Refer to [ChestXRayEnsembling](https://github.com/edoardogiacomello/ChestXRayEnsembling).

**Article**<details>
  <summary> 
  Image embeddings extracted from CNNs outperform other transfer learning approaches in chest radiographs’ classification.
  </summary>
  Noemi Gozzi, Edoardo Giacomello, Martina Sollini, Margarita Kirienko, Angela Ammirabile, Pierluca Lanzi, Daniele Loiacono, Arturo Chiti. Image embeddings extracted from CNNs outperform other transfer learning approaches in chest radiographs’ classification. Pre-Print.
</details>

### 6.3 Transfer Learning via Adversarial Networks 

See [SegAN-CAT](https://github.com/edoardogiacomello/SegAN-CAT).

**Article**<details>
  <summary> 
  Brain mri tumor segmentation with adversarial networks.
  </summary>
  Edoardo Giacomello, Daniele Loiacono, and Luca Mainardi. Brain mri tumor segmentation with adversarial networks. In 2020 International Joint Conference on Neural Networks (IJCNN), pages 1–8. IEEE, 2020
</details>

### 6.4 Addressing Data Heterogeneity using Generative Adversarial Networks 
**Code**: See [Brain-MRI-generation-using-GANs](https://github.com/edoardogiacomello/Brain-MRI-generation-using-GANs) 

**Article**<details>
  <summary> 
  Brain magnetic resonance imaging generation using generative adversarial networks.
  </summary>
  Emanuel Alogna, Edoardo Giacomello, and Daniele Loiacono. Brain magnetic resonance imaging generation using generative adversarial networks. In 2020 IEEE Symposium Series on Computational Intelligence (SSCI), pages 2528–2535. IEEE, 2020.
</details>



