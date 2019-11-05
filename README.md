# Stock prediction based on stock indicators with LSTM and stock-affecting news with BERT WWM
This is the repository of COMP90019 Distributed Computing Project.  
Language: python
Key library:
hanlp
pytorch
pytorch_transformers



## Team Members
Tong He		  867488  
Yao Wang		869992  
Supervisor: Richard Sinnott

## introduction
There are two models in this repository. Code and result are shown as ipython notebook.
# Model I
A hybrid model that combines LSTM and MLP to predict stock.  
data_index_2.ipynb  
Contains definitions and related methods of the Getdata class for reading and preprocessing data. We provide a copy of processed test data and dev data for the model (train_getdata.pkl,dev_getdata.pkl,test_getdata.pkl).  
model_index_2.ipynb  
Include the defination of our model and related functions. A sample of trained model is saved in .bin.  
evaluate_index.ipynb  
Contains predefined function for test and show result.  
main_index_v1.ipynb  
Main file of Model I，which control the entire process of the project, from data generation to training to evaluation.
If '*_getdata.pkl' are given, set "new_data" parameter to False to skip regenerate dataset.

# Model II  
This is the text classifier for stock related news.
bertWWM_classifier.ipynb  
Include whole process(data collection,training,evaluation) of this model. Our program is based on PyTorch platform. For the use of the Bert-WWM pre-training model, and the conversion between TensorFlow and PyTorch, please refer to the following two github.  
https://github.com/ymcui/Chinese-BERT-wwm  
https://github.com/huggingface/transformers  
'Construct dataset' cells can be skipped when .csv is given.
