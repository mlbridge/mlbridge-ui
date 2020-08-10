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




