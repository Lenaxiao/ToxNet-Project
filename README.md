# ToxNet

ToxNet is a data science group from DIRECT program at the University of Washington, which also collaborates with PNNL. The research is to predict the toxicity of various chemicals based on their structures. We utilize the published dataset from U.S Department of Health and Human Services' National Toxicology Program (https://ntp.niehs.nih.gov/pubhealth/evalatm/test-method-evaluations/acute-systemic-tox/models/index.html) and convert those tabular data into image and text file applying Open-Source Cheminformatics Software [RDKit] (http://www.rdkit.org). Furthermore, we fit these different format of data into three different neural networks: RNN (text), CNN (image) and MLP (tabular). Our primary goal is to analyze whether these models provide similar prediction and if there is a model that performs consistently better than others.

---

### Description of Models

#### MLP

Generally, multilayer perceptron (MLP) performs well to train the tabular form of data. We adopted this strategy for our project. In this network, we tuned the hyperparameters including dropout rate, number of layers, activation function (relu_type), number of nodes per layer, regulization type and regulization value.

|               | dropout rate | number of layer | relu_type | Nodes | regulization | regulization value |
| ------------- | ------------ | ----------------| ----------| ----- | ------------ | ------------------ |
|    nontoxic   | 
|    verytoxic  |
|    GHS        |
|    EPA        |
|    LD50       |


#### RNN

|               | em_dim | relu_type | conv_units | reg_type | reg_value | num_layer | layer_units | val_AUC/RMSE | test_AUC/RMSE |
| ------------- | ------------ | ----------------| ----------| ----- | ------------ | ------------------ |
|    nontoxic   | 
|    verytoxic  |
|    GHS        |
|    EPA        |
|    LD50       |

#### CNN



---

### Files Setup
* The functions are in chem_scripts folder.
* The modules folder provides all the executable files. `MLP_Prototype.py` includes code for training, prediction and recording results. The rest of `.py` files are for data cleaning and data extraction.
* The data directory records all the useful data.

---

### Dependencies

* numpy
* pandas
* seaborn
* sklearn
* tensorflow (GPU backend)
    * _You need to install CUDA (>= 7.0, version 9 recommended) and cuDNN (>=v3, version 7 recommended)_
* keras
* RDKit

---

### Installation
* $ pip install numpy==1.14.4
* $ pip install pandas==0.23.1
* $ pip install seaborn==0.8.1
* $ pip install -U scikit-learn==0.19.1
* $ pip install tensorflow-gpu==1.8.0
    * _follow instructions in tensorflow website to install CUDA and cuDNN (https://www.tensorflow.org/install/install_sources)_
* $ pip install Keras==2.2.0
* $ conda create -c rdkit -n my-rdkit-env rdkit (version 2017.09.1)

---

### Acknowledgments

Special thanks to Garrett Goh’s careful and patient guidance on our project and amazing support form  Pro. Jim Pfaendtner and Pro.Dave Beck.
