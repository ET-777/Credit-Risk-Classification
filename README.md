Credit Risk Classification
-----------------------

Deepn neural network to predict whether a customer from a credit and transaction datasets is of high or low risk. A binary model is trained with tensorflow after processing the data. Datset is [here](https://www.kaggle.com/datasets/praveengovi/credit-risk-classification-dataset). You can see the data processing, model, code, and full explanations in the `CreditRiskClassification.ipynb` notebook above.

Quick Overview
----------------------

The dataset consists of two dataframes. A dataframe with customer demographic features that have been numbered and encoded. A label of 1 is for high risk customers and 0 for low risk. The second dataframe is of customer transactions for certain products. OVD features in this data indicate overdue payment types. Customer data has 1125 customers that matches the number of unique customers in the transactions dataframe, however this dataframe has over 8k transactions.

<p align="center">
<br />
Customer Data
<br />
<br />
<img src="https://github.com/ET-777/Credit-Risk-Classification/blob/master/images/customers.jpg"/>
<br />
<br />
<br />
Transactions Data
<br />
<br />
<img src="https://github.com/ET-777/Credit-Risk-Classification/blob/master/images/payments.jpg"/>
<br />
<br />
<br />
</p>

After joining the datasets, getting rif of the unecessary featrures and filling null values, we have a dataset to train the model with.

<p align="center">
<br />
<br />
<img src="https://github.com/ET-777/Credit-Risk-Classification/blob/master/images/data.jpg"/>
<br />
<br />
<br />
</p>

The model was constructed sequentially. Three Dense layers with relu activations, a dropout layer to reduce overgfittinh, and an output layer with a sigmoid activation.

<p align="center">
<br />
Model
<br />
<br />
<img src="https://github.com/ET-777/Credit-Risk-Classification/blob/master/images/model.jpg"/>
<br />
<br />
<br />
</p>

Results
----------------------

The model was trained for 10 epoch with a Binary Crossentropy loss function and a learning rate of 0.003 with adam optimizer. Data was also split by 30% for testing.
<br /><br />
 Data | Loss | Acc
------------ | ------------- | -------------
Training | 0.4609 | 0.83
Testing | 0.4342 | 0.84

<br /><br />
The loss function and accuracy results of both the training and validation data is close and similar. This means our model did not overfit the traing data and generalizes well new examples. With a loss function of 0.43 and an accuracy of 0.84 for our validation data, we have a good model.

Installation
----------------------

### Download the data

* Clone this repo to your computer.
* Create a `Data` folder in the project directory
* Download the data files from Kaggle into the `Data` folder.  
    * You can find the data [here](https://www.kaggle.com/datasets/praveengovi/credit-risk-classification-dataset).
    * You'll need to register with Kaggle to download the data.
* Extract the `.zip` file you downloaded into the `Data` folder.

### Install the requirements
 
* Install the requirements with `anaconda` or with pip using `pip install -r requirements.txt`.
    * Make sure you use Python 3.
    * You may want to use a virtual environment for this.

Usage
-----------------------

* Open `CreditRiskClassification.ipynb` with `Jupyter Notebook`.
* Run the notebook
    * Make sure you are running `tensorflow` with a `GPU`.
