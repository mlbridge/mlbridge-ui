# MLBridge-UI

This repository contains the user interface for the MLBridge Project. It allows 
the user to customise it as per his/her requirement for any other project, for 
example genomics, computer vision etc. Currently, it is being used for domain 
name cybersecurity.

## Installation

Clone the repository:
```
git clone https://github.com/mlbridge/mlbridge-ui.git
```

Go to the `mlbridge-ui` directory and install the dependencies:
```
cd mlbridge-ui
pip install -r requirements.txt
```

Install Elasticsearch by following the instructions from this 
[link](https://phoenixnap.com/kb/install-elasticsearch-ubuntu). Start the 
Elasticsearch server and then run the `ui.py` app:
```
cd mlbridge-ui/mlbridge-ui/src
python3 ui.py
```

## Features:

This repository contains code for a user interface for the purposes of domain 
name cybersecurity. The three main features of the application are:

- Historical Analysis: The application allows the user to historically analyse
the frequency at which domains have been queried and the IP addresses of the 
users querying those domains
- Manual Vetting: The application allows a user to manually vet domain names
(classify them as benign or malicious) that the machine learning model is not 
confident about.
- Retraining the Model: The application allows the user to retrain the machine 
learning model that is used to classify domain names as malicious or benign and 
obtain the analytics for the same.

### Historical Analysis

A demo of the application can be seen below:

<p align = "center">
    <img style="float: right;" src="https://github.com/chanakyaekbote/coredns_ml_plugin/blob/master/readme_assets/dash_app_gif.gif">
</p>

There are three main use cases for having a historical analysis:

- Domain Name Analysis: The application allows the user to search for a
a particular domain name along with a request time range. The application will 
then search for that particular domain name in the Elasticsearch database. Once the 
domain name is found, the app will display the number of requests to that 
particular domain name in that time range, the nature of the domain name 
(benign or malicious) and also the IP addresses that have queried that 
particular domain name. This allows for a domain specific analysis.


<p align = "center">
  <img src="https://github.com/chanakyaekbote/coredns_ml_plugin/blob/master/readme_assets/domain_name_app_1.PNG" 
  width="700"/> 
</p>

- Analysis of Malicious Domain Names: The application allows the user to
visualize the top 20 malicious domains queried, as a bar graph. It also displays 
a list of all the malicious domains queried which can be seen via a toggle
switch in the same window. This allows the user to gain a general picture of all
the malicious domain names queried and also helps in identifying model 
misclassification.

<p float="left" align = "center">
  <img src="https://github.com/chanakyaekbote/coredns_ml_plugin/blob/master/readme_assets/malicious_app_1.PNG" 
  width="400"/>
  <img src="https://github.com/chanakyaekbote/coredns_ml_plugin/blob/master/readme_assets/malicious_app_2.PNG" 
  width="400"/>
</p>

- Analysis of Benign Domain Names: The application allows the user to
visualize the top 20 benign domains queried, as a bar graph. It also displays 
a list of all the benign domains queried which can be seen via a toggle
switch in the same window. This allows the user to gain a general picture of all
the benign domain names queried and also helps in identifying model 
misclassification.

<p float="left" align = "center">
  <img src="https://github.com/chanakyaekbote/coredns_ml_plugin/blob/master/readme_assets/benign_app_1.PNG" width
  ="400"/>
  <img src="https://github.com/chanakyaekbote/coredns_ml_plugin/blob/master/readme_assets/benign_app_2.PNG" width
  ="400"/>
</p>


### Manual Vetting


A demo of the application can be seen below:

<p align = "center">
    <img style="float: right;" src="https://github.com/cekbote/coredns_ml_plugin/blob/master/readme_assets/manual_vetting.gif">
</p>

Manual Vetting allows the user to manually vet domain names that the model has 
a low confidence on, thereby creating a new dataset of malicious or benign 
domains. This dataset can be used for blocking or allowing domains and also for 
updating the dataset for retraining the model. 

<p align = "center">
  <img src="https://github.com/cekbote/coredns_ml_plugin/blob/master/readme_assets/manual_vetting_screenshot.PNG" 
  width="700"/> 
</p>


### Retraining the Model

The machine learning model would have to be retrained when there is new data or 
the model is underperforming. The model can be retrained via the `training` tab.

The accuracy and loss graphs are updated in real time while the model is being 
trained.

<p float="left" align = "center">
  <img src="https://github.com/mlbridge/mlbridge-ui/blob/master/readme-assets/accuracy_graph.jpg" width
  ="550"/>
  <img src="https://github.com/mlbridge/mlbridge-ui/blob/master/readme-assets/loss_graph.jpg" width
  ="550"/>
</p>

Once the training is complete, the model efficacy can be judged by looking at 
the confusion matrices as well as the confusion metrics.

<p align = "center">
  <img src="https://github.com/cekbote/coredns_ml_plugin/blob/master/readme_assets/manual_vetting_screenshot.PNG" 
  width="700"/> 
</p>


