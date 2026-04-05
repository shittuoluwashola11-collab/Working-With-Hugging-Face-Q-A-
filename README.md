# Working-With-Hugging-Face-Q-A-
An automated Question-Answering (QA) system that utilizes the Hugging Face Transformers library and pypdf to extract and query information from employee policy documents.
# Policy-QA: AI-Powered Document Query System

[cite_start]An automated solution for extracting text from corporate policy documents and performing precise Question-Answering (QA) using Natural Language Processing. 

## 🚀 Overview
[cite_start]This project demonstrates how to use the `distilbert-base-cased-distilled-squad` model to parse unstructured PDF data and return specific answers to user queries.  [cite_start]The system is currently configured to analyze US Employee Policy documents. 

## 🛠️ Technical Stack
* [cite_start]**Language:** Python 3.8.10 
* [cite_start]**PDF Parsing:** `pypdf` 
* [cite_start]**NLP Framework:** `transformers` (Hugging Face) 
* [cite_start]**Model:** `distilbert-base-cased-distilled-squad` 

## 📋 Features & Policy Extraction
The system is capable of extracting and answering questions regarding:
* [cite_start]**Vacation Policy:** 25 days entitlement annually. 
* [cite_start]**Sick Leave:** Up to 10 days per year. 
* [cite_start]**Notice Period:** 2-week requirement for resignations. 
* [cite_start]**Maternity/Paternity:** 16 weeks maternity leave and 10 days paternity leave. 
* [cite_start]**Remote Work:** Policy allows for up to 2 days per week. 
* [cite_start]**Probation:** Standard 3-month period for new hires. 

## 💻 Usage
[cite_start]To use the QA system, load the notebook and provide a question as shown below: 

```python
from pypdf import PdfReader
from transformers import pipeline

# 1. Load the PDF
reader = PdfReader("Employee Policy.pdf")

# 2. Extract and Query
question = "How may public holiday does the company observe?"
# Result: 12 public holidays annually
