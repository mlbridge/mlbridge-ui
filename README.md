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
