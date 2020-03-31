# BreastCancerDetector - an API that predicts malignancy based on features of biopsied breast cells.

## Introduction 
**Descriptions of the Data Challenge**
You belong to the data team at a local research hospital. You've been tasked with developing a means to help doctors diagnose breast cancer. You've been given data about biopsied breast cells; where it is benign (not harmful) or malignant (cancerous).

- What features of a cell are the largest drivers of malignancy? Build a model that predicts whether a given biopsied breast cell is benign or malignant.
- What features drive your false positive rate for your model you derived above, what features drive your false negative rate? 
- How would a physician use your product?
- There is a non-zero cost in time and money to collect each feature about a given cell. How would you go about determining the most cost-effective method of detecting malignancy?

**The final product**:
BreastCancerDetector is an **API** that will return the prediction based on the input cell parameters. 

Example input: 
```
curl -d '{ "ID": 752904, "Clump Thickness": 10, "Uniformity of Cell Size": 1, "Uniformity of Cell Shape": 1, "Marginal Adhesion": 1, "Single Epithelial Cell Size": 2, "Bare Nuclei": 10, "Bland Chromatin": 5, "Normal Nucleoli": 4, 'Mitoses': 1 }' http://127.0.0.1:5000
```
Example output: 
```
{ "Prediction": "Benign", "Confidence": 97.34% }
```
The predictions are saved in a timestamped json file under the folder "Output". 
Example file name: "predictions_03182020_1616.json". Timestamp: MonthDayYear_HourMinute

**Instructions to run the API**
* clone the repo to local machine
* cd to the folder
* In the terminal, run python api.py
* In a separate terminal, test with sample input as described above

# The Data
9 features (all range from 1-10) + Class (4 for benign, 2 for malignant)

Clump Thickness, Uniformity of Cell Size, Uniformity of Cell Shape, Marginal Adhesion, Single Epithelial Cell Size, Bare Nuclei, Bland Chromatin, Normal Nucleoli, Mitoses


