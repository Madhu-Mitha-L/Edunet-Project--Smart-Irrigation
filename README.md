# 🌿 Smart Irrigation System - AICTE Internship (Cycle 2)

## Table of Contents

- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Proposed Solution](#proposed-solution)
- [Architecture](#architecture)
- [Tech Stack Used](#tech-stack-used)
- [Installation Steps](#installation-steps)
- [How to Run](#how-to-run)
- [Model Overview](#model-overview)
- [Features](#features)
- [Sample Use Case](#sample-use-case)
- [Output](#output)
- [Future Scope](#future-scope)
- [Acknowledgements](#acknowledgements)
- [File Structure](#file-structure)

## Problem Statement
Water scarcity is a major global concern. Traditional irrigation systems waste a significant amount of water due to lack of automation. This project aims to develop a **Smart Irrigation System** using AI to automate sprinkler control based on sensor data.

## Objectives
- Predict whether individual sprinkler parcels should be ON or OFF using AI.
- Minimize water usage and optimize irrigation based on environmental conditions.
- Enable real-time predictions through a user-friendly interface.

## Proposed Solution
We developed a machine learning model that takes in 20 scaled sensor values (between 0 and 1) and predicts the status (ON/OFF) of 20 sprinkler parcels. A Streamlit app was created for easy interaction.

## Architecture
1. Data Preprocessing & Model Training (`.ipynb`)
2. Model saved using Joblib (`Farm_Irrigation_System.pkl`)
3. Streamlit App for UI (`app.py`)


```



             ┌────────────────────────────┐
             │  Sensor Data Collection    │
             └────────────┬───────────────┘
                          │
                          ▼
             ┌────────────────────────────┐
             │  Data Preprocessing        │
             │  (Scaling, Cleaning, etc.) │
             └────────────┬───────────────┘
                          │
                          ▼
             ┌────────────────────────────┐
             │  Model Training            │
             │  (e.g., Random Forest)     │
             └────────────┬───────────────┘
                          │
                          ▼
             ┌────────────────────────────┐
             │  Save Trained Model        │
             │  using Joblib              │
             │  → Farm_Irrigation_System.pkl │
             └────────────┬───────────────┘
                          │
                          ▼
             ┌────────────────────────────┐
             │  Build Frontend using      │
             │  Streamlit (`app.py`)      │
             └────────────┬───────────────┘
                          │
                          ▼
             ┌────────────────────────────┐
             │  Predict Sprinkler Status  │
             │  (ON/OFF for 20 zones)     │
             └────────────────────────────┘

```
## Tech Stack Used
- Python
- Scikit-learn
- Streamlit
- Jupyter Notebook
- NumPy, Pandas
- Joblib

## Installation Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/smart-irrigation.git
   cd smart-irrigation
## How to Run
**streamlit run app.py**

## Model Overview

- **Input**: 20 scaled values representing sensor readings (range: 0 to 1)  
- **Output**: 20 binary values (0 = OFF, 1 = ON) representing sprinkler status  
- **Model Type**: *(e.g., Random Forest, Logistic Regression – mention the actual model used)*

---

## Features

- ✅ Real-time prediction of sprinkler status  
- ✅ Simple and interactive web interface (Streamlit)  
- ✅ Accepts 20 sensor inputs via sliders  
- ✅ Predicts ON/OFF for each sprinkler zone  
- ✅ Efficient water management and crop health support  

---

## Sample Use Case

A farmer uses the app to input sensor values such as moisture, temperature, and humidity. The model then predicts which sprinkler zones need to be activated, helping the farmer save water while ensuring crops receive adequate irrigation.

---
## OUTPUT
**INPUT INTERFACE**
<img width="1918" height="1012" alt="image" src="https://github.com/user-attachments/assets/5d04e8fc-a4a7-4741-ba4a-cab03e742cc6" />
<img width="1915" height="1005" alt="image" src="https://github.com/user-attachments/assets/15f0eacd-d03c-4218-aa58-c3ac26d18472" />
<img width="1913" height="938" alt="image" src="https://github.com/user-attachments/assets/2ead5a87-1b85-4329-adbf-c4fb55e65cb9" />

**PREDICTED OUTPUT**
<img width="1397" height="276" alt="image" src="https://github.com/user-attachments/assets/c9c62a25-5352-477c-9919-a9a3e5c91115" />

## Future Scope

- 🔗 Integrate with IoT devices for real-time sensor data  
- 🌧️ Include weather forecasting and soil type data  
- 🤖 Enable automatic control of sprinklers  
- ☁️ Cloud deployment with mobile app support  
- 📊 Maintain historical data for performance tracking  

---

## Acknowledgements

- [Edunet Foundation](https://www.edunetfoundation.org/)  
- [Shell India](https://www.shell.in/)  
- [AICTE](https://www.aicte-india.org/)  
- Mentors: Hariharan, Aryan, Nikita, and the entire support team  

---

## File Structure

```bash
📦 smart-irrigation/
├── app.py                      # Streamlit web app
├── Farm_Irrigation_System.pkl  # Trained model
├── Week 3 task.ipynb           # Jupyter Notebook (model training)
└── README.md                   # Project documentation
