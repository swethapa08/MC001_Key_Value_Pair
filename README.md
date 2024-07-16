# Key-Value Pair Identification Using Graph Theory(Code : MC001)

## Introduction
  The MC001 assignment focuses on the application of graph theory and machine learning to extract, visualize, and predict key-value pairs from unstructured data. By utilizing Optical Character Recognition (OCR), text pre-processing, Named Entity Recognition (NER), and 
machine learning techniques, the project generates a graph highlighting relationships between key-value pairs in a sample bill image and predicts the accuracy of these relationships. This feature is integrated into a mobile application, allowing users to interactively 
highlight key-value pairs within unstructured data.

## Objective
  The primary objective is to develop a system that accurately identifies, visualizes, and predicts key-value pairs from an unstructured data using graph theory and machine learning. 
  The goals include:

* Extracting text from an image using OCR.
* Pre-processing the extracted text for analysis.
* Applying NER(Stanza) to identify key-value entities.
* Generating a graph to represent relationships between identified key-value pairs.
* Using machine learning to predict the accuracy of these relationships.
* Integrating the graph visualization and prediction feature into a mobile
application.

## Concept of Graph Creation
**To describe the structure and relationships within the Schenker transactions dataset, we store the values of Shipment number in class Pkey(Primary Key) as the marker entity. The Shipper as the Stent(Strong Entity) class and Consignee in Wkent(Weak Entity) class. Both classes Stent and Went are linked to Key entity each Wkent object depends on one or more Stent objects. From the given Stent and Went attributes we can plot various regression plots to predict the trends of the given data. 
The given structure uses the concept of forest to organise the data, each table is organised as a tree with defined relationships with one another and build a forest with relationships defined for separate trees.**

## Snippet of Class Structure for Graph 
```
class Pkey:
    def __init__(self):
        self.arr = []
        self.label = ''
class Stent(Pkey):
    def __init__(self, tag, arr1):
        super().__init__()
        self.tag = tag
        self.arr1 = arr1
        self.stent = {}
        for i in range(len(tag)):
            self.stent[tag[i]] = arr1[i]
class Wkent(Pkey):
    def __init__(self, tag, arr2):
        super().__init__()
        self.tag = tag
        self.arr2 = arr2
        self.wkent = {}
        for i in range(len(tag)):
            self.wkent[tag[i]] = arr2[i]
if __name__=="main":
     //create and display an instance of Stent, Wkent
```

## Challenge Example
Consider a sample bill image containing various key-value pairs such as:

* Date: 2023-07-15
* Total Amount: $250.00
* Vendor: ABC Store
* Item List:
   1. Item1: $50.00
   2. Item2: $200.00
The challenge is to accurately extract these key-value pairs, pre-process the data,
recognize entities, generate a graph that represents the relationships between these
pairs, and predict the accuracy of these relationships using machine learning.

## Technological Requirements
* OCR Technology: Tesseract OCR
* Text Pre-processing Tools: NLTK
* NER Tools: Stanza
* Graph Theory Libraries: Network, Matplotlib and Ploty
* Machine Learning Libraries: Scikit-learn, TensorFlow, Random Forest Regression
* Mobile Application Development Tools: React Native

## System Specifications
* Processor: Minimum quad-core processor
* RAM: Minimum 8GB
* Storage: Minimum 256GB SSD
* Operating System: Windows 7 or macOS 10.
* Development Environment: Python 3.8+, Android Studio/React Native

## Expected Outcomes
1. Successful extraction of text from sample bill images.
2. Effective pre-processing and normalization of the extracted text.
3. Accurate identification of key-value pairs using NER.
4. Generation of a graph that correctly represents relationships between key-value
pairs.
5. Prediction of the accuracy of these relationships using machine learning.
6. Integration of the graph visualization and prediction feature into a mobile
application through lens.
