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

## About

This repository contains code for a user interface for the purposes of domain 
name cybersecurity. The user can perform three main actions:

1) Get the analysis of how many times and at what frequency a particular domain 
name was queried.
2) Manually vet certain domain names and classify them as malicious or benign.
3) Retrain the machine learning model that is used to classify domain names as
malicious or benign and obtain the analytics for the same.


