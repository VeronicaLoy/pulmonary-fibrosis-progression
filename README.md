# Pulmonary Fibrosis Prediction

# Introduction

Artificial Intelligence and Machine Learning has been used in the Medical field from the early 70s, when AI itself was only 15 years old, since then AI has been used to assist medical professionals to make informed decisions where they would not normally be able to identify root causes. One such case would be in fibrotic lung disease progression prediction, which this project aims to solve. Using patient information and CT scans and processed through an ensemble of neural networks and traditional machine learning techniques , the application will return clinicians a prediction of the progression of the patient's lung function decline via the proxy of forced vital capacity or FVC.


# Getting Started 


Ensure you have [conda](https://docs.conda.io/en/latest/miniconda.html) installed.
Execute the following commands in terminal to run the application locally. The commands below clones this repository, and install all the necessary packages in a new environment named 'fibrosis', before starting the application in http://localhost:8501/.

Administrator privilages may be required to run the app. This can be done by running Anaconda prompt as an administrator on Windows.

```
# clone this repository
git clone https://github.com/VeronicaLoy/pulmonary_fibrosis_progression.git

cd pulmonary-fibrosis-progression

conda create -n fibrosis python=3.6.7
conda activate fibrosis
pip install -r requirements.txt

streamlit run app.py
```

The app requires patient details to be indicated, and a zip folder containing CT scans of patients lungs in to be uploaded before prediction. The CT scans has to be in .dcm format. A sample of this zip folder of .dcm images can be found under `sample dataset` folder.


Alternatively, you can access the app [here](http://54.186.100.151:8501/). Due to hosting limitations, the publicly hosted model is a simplied version, which contains three out of four models in the ensemble - the MLP model, EfficientNet model, and Huber Linear model (see section on About the Model below for more information). The application will be hosted on at the aforementioned link for a period of 2 months, till 31st December 2020.



 < insert gif here to show uploading and toggling of app>






# About the Model

The system consists of 4 machine learning sub-models and an ensemble model which aggregates the results and determines the final output. Using this private dataset [here](https://www.kaggle.com/c/osic-pulmonary-fibrosis-progression/data), the ensemble achieved a laplace log likelihood of -6.87. The four models are as follows. The architecture is illustrated below.

- MLP model
- EfficientNet model
- Huber linear model
- CNN model



 < insert system architecture here to show uploading and toggling of app>
