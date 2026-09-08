# AI-Based Smart Energy Consumption Forecasting & Advisor

An AI-based energy management project that uses Machine Learning to forecast energy consumption, identify unusual usage patterns, and provide simple recommendations for more efficient energy use.

This project was developed as part of the **1M1B AI for Sustainability Virtual Internship**, in collaboration with **IBM SkillsBuild & AICTE**.

<img width="1920" height="1080" alt="Screenshot (63)" src="https://github.com/user-attachments/assets/9c1dd969-a449-4923-ab2b-72f3412f9b12" />

## 🌱 Project Overview

Energy consumption is increasing in homes, offices, educational institutions, and other buildings. However, users often do not have a simple way to understand their consumption patterns or identify periods of unusually high energy usage.

This project uses historical energy consumption data and factors such as:

* Occupancy
* Temperature
* Hour of the day
* Day of the week
* Peak-hour information
* Previous energy consumption

The system uses Machine Learning to forecast energy consumption and provides simple insights and recommendations to help users understand and manage their energy usage.

---

## 🎯 Problem Statement

**How might we use AI to predict energy consumption and identify high or unusual usage patterns so that energy can be used more efficiently and sustainably?**

---

## 🌍 SDG Alignment

### Primary SDG

**SDG 7 – Affordable and Clean Energy**

### Other Relevant SDGs

* **SDG 12 – Responsible Consumption and Production**
* **SDG 13 – Climate Action**

The project supports better energy awareness, responsible consumption, and sustainable energy management.

---

## 🤖 AI & Machine Learning Approach

The project follows this workflow:

```text
Energy Data
     ↓
Data Preprocessing
     ↓
Feature Engineering
     ↓
Exploratory Data Analysis
     ↓
Machine Learning Models
     ↓
Model Evaluation
     ↓
Energy Consumption Prediction
     ↓
Anomaly Detection
     ↓
Smart Energy Advisor
     ↓
Interactive Dashboard
```

### Machine Learning Models

Three regression models were tested:

1. **Linear Regression**
2. **Gradient Boosting Regressor**
3. **Random Forest Regressor**

The models were compared using:

* MAE – Mean Absolute Error
* RMSE – Root Mean Squared Error
* R² Score

### Best Performing Model

**Random Forest Regressor**

Test performance:

| Metric   | Score |
| -------- | ----: |
| MAE      |  1.77 |
| RMSE     |  2.25 |
| R² Score | 0.958 |

The results may vary slightly depending on the data generation and execution environment.

---

## 🔍 Anomaly Detection

The project also uses **Isolation Forest** to identify unusual energy consumption patterns.

In the current prototype:

* Total records: **8,760**
* Normal records: **8,584**
* Unusual records: **176**

These unusual records can help users investigate periods where energy consumption differs significantly from normal patterns.

---

## 📊 Important Features

The model considers several factors that can influence energy consumption.

The most important features in the current model were:

| Feature                  | Importance |
| ------------------------ | ---------: |
| Occupancy                |      0.798 |
| Previous Day Consumption |      0.076 |
| Temperature              |      0.037 |
| Peak Hour                |      0.034 |
| Day of Week              |      0.019 |

Occupancy was the strongest feature in the current dataset, showing how strongly energy demand can be related to the number of people using a building.

---

## 💡 Smart Energy Advisor

The Smart Energy Advisor combines the predicted energy consumption with usage conditions to provide simple recommendations.

For example, it can identify:

* Normal energy usage
* Moderate energy usage
* High energy usage
* Possible unusual consumption

It can then provide suggestions such as checking unnecessary loads, reviewing peak-hour consumption, or reducing avoidable energy usage.

---

## 🖥️ Interactive Dashboard

A web-based dashboard was developed using **Gradio**.

The dashboard includes:

* 🔮 Energy Consumption Prediction
* 📊 Energy Usage Analytics
* 🤖 Machine Learning Model Performance
* 🔍 Feature Importance
* 📁 Project Information
* 🛡️ Responsible AI Considerations

The dashboard is designed to make the project easier to understand for users who may not have a technical Machine Learning background.

---

## 🛠️ Technologies Used

* **Python**
* **Google Colab**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Gradio**
* **GitHub**

---

## 📂 Project Structure

```text
AI-Smart-Energy-Consumption-Forecasting-Advisor/
│
├── AI_Smart_Energy_Consumption_Forecasting_Advisor.ipynb
├── README.md
├── requirements.txt
├── data/
│   └── energy_consumption.csv
│
├── screenshots/
│   ├── dashboard.png
│   ├── model_performance.png
│   ├── feature_importance.png
│   └── energy_analysis.png
│
└── results/
    └── model_results.csv
```

*The exact structure may vary depending on the files included in the repository.*

---

## 🚀 How to Run

### Option 1 – Google Colab

1. Open the project notebook.
2. Upload/open it in Google Colab.
3. Run the cells from top to bottom.
4. The dataset will be generated and processed.
5. The ML models will be trained and evaluated.
6. Launch the Gradio dashboard.
7. Use the dashboard to test energy predictions and view analytics.

### Option 2 – Local Setup

Clone the repository:

```bash
git clone https://github.com/Prathmg/AI-Based-Smart-Energy-Consumption-Forecasting-Advisor.git
cd AI-Based-Smart-Energy-Consumption-Forecasting-Advisor
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Run the notebook using Jupyter Notebook or JupyterLab.

---

## 📈 Current Dataset

The current prototype uses **synthetic hourly energy consumption data for one year**, containing **8,760 records**.

The dataset includes variables such as:

* Date and time
* Temperature
* Occupancy
* Hour
* Day of week
* Month
* Weekend information
* Peak-hour information
* Previous-hour consumption
* Previous-day consumption
* Energy consumption

### Important Note

The current dataset is **simulated/synthetic data** created for developing and testing the prototype. It is not presented as real electricity-meter data.

Using real smart-meter or building energy data would be the next step toward real-world deployment.

---

## 🛡️ Responsible AI

Responsible AI was considered during the development of the project.

### Transparency

The project uses measurable ML evaluation metrics such as MAE, RMSE, and R² to evaluate model performance.

### Data Privacy

The prototype does not use personal or individually identifiable user data.

### Responsible Recommendations

The system provides recommendations as decision-support information rather than claiming that every recommendation is universally correct.

### Limitations

The current model is trained and tested using synthetic data. Its performance on real-world energy data may be different.

---

## 🎯 Target Users

The project can be useful for:

* 🏠 Households
* 🏫 Educational institutions
* 🏢 Offices
* 🏭 Small organizations
* 👨‍💼 Facility managers
* 🎓 Students and researchers
* 🌱 People interested in energy conservation

---

## 🌟 Expected Impact

The project aims to help users:

* Understand energy consumption patterns
* Forecast future energy demand
* Identify unusual consumption
* Recognize high-demand periods
* Make better energy-management decisions
* Reduce unnecessary energy usage
* Improve awareness about sustainable energy consumption

Actual electricity or cost savings have **not yet been measured**, because the current version is a prototype using synthetic data.

---

## 🔮 Future Scope

The project can be improved by:

* Connecting real-time smart-meter data
* Adding electricity tariff and cost prediction
* Integrating renewable energy generation data
* Adding solar PV generation forecasting
* Developing a mobile-friendly interface
* Adding real-time alerts for abnormal consumption
* Deploying the system on cloud infrastructure
* Using real building or campus energy data
* Adding a conversational AI assistant for energy-related questions

---

## 🎓 Internship Context

This project was developed as part of the:

**1M1B AI for Sustainability Virtual Internship**

In collaboration with:

* **1M1B**
* **IBM SkillsBuild**
* **AICTE**

The project focuses on applying AI and Machine Learning to a sustainability-related problem aligned primarily with **SDG 7 – Affordable and Clean Energy**.

---

## 👨‍💻 Author

**Prathmesh**

Electrical Engineering | Power Systems | Machine Learning | AI for Sustainability

---

## 📌 Project Status

**Prototype Completed**

The current version demonstrates the complete workflow from data generation and preprocessing to ML prediction, anomaly detection, energy recommendations, and an interactive dashboard.

---

## 📄 License

This project is created for educational and internship purposes.
