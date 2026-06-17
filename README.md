# genai-customer-insights-nlp

**Applying Generative AI and pre-trained Transformer models to analyze customer service logs, uncovering insights in sentiment, issue patterns, and response quality to enhance customer interaction strategies.**

---

## 📌 Project Overview

This project analyzes customer service conversation logs from **Fresh Fare Meal Kits** using **Generative AI (GenAI)** and **pre-trained NLP models** from the Hugging Face Transformers library. The goal is to extract actionable insights from 20 real call logs, enabling data-driven improvements to customer interaction protocols.

The project was developed for the **QuickServe Meals Analytics Team** as part of a broader customer experience enhancement initiative.

---

## 🎯 Objectives

- Apply Generative AI models (Google's **FLAN-T5**) to analyze text and conversation data
- Gain proficiency in utilizing pre-trained NLP models from the **Transformers library**
- Understand how generative AI models learn from data to generate new content
- Design and develop AI-driven solutions to solve complex problems in **customer service**

---

## 📂 Repository Structure

```
genai-customer-insights-nlp/
│
├── Call_Logs.csv                    # Raw dataset: 20 customer service call logs
├── gen_ai_customer_insights.ipynb   # Main Jupyter Notebook (all 5 tasks)
├── requirements.txt                 # Python dependencies
└── README.md                        # Project documentation
```

---

## 📊 Dataset

| Property         | Detail                                      |
|------------------|---------------------------------------------|
| **File**         | `Call_Logs.csv`                             |
| **Records**      | 20 customer service conversation logs       |
| **Structure**    | Single `Logs` column (unstructured text)    |
| **Date Range**   | April 3 – April 29, 2024                    |
| **Company**      | Fresh Fare Meal Kits                        |

Each log entry contains:
- **Date** and **Time** of the call
- **Agent name** and **Client name**
- Full **dialogue** from greeting to resolution

---

## 🛠️ Tech Stack

| Tool / Library      | Purpose                                   |
|---------------------|-------------------------------------------|
| Python 3.12         | Core programming language                 |
| pandas              | Data loading and manipulation             |
| Transformers        | Pre-trained NLP models (Hugging Face)     |
| google/flan-t5-base | Conversation summarization & reason extraction |
| MoritzLaurer/multilingual-MiniLMv2-L6-mnli-xnli | Zero-shot cancellation detection |
| matplotlib          | Plotting and visualization                |
| wordcloud           | Word cloud generation                     |

---

## 📋 Task Breakdown

### Task 1: Clean and Prepare Data
Transform unstructured call logs into a structured DataFrame by extracting:
- Date, Time, Agent, Client, and Conversation columns

### Task 2: Automated Conversation Summarization
Use `google/flan-t5-base` to generate concise summaries of each customer conversation, capturing the main points discussed.

### Task 3: Detecting Cancellation Requests
Apply zero-shot classification (`MoritzLaurer/multilingual-MiniLMv2-L6-mnli-xnli`) to flag conversations that contain cancellation requests — labelled as `cancellation` or `other`.

### Task 4: Identifying Cancellation Reasons
For flagged cancellation conversations, use FLAN-T5 to extract the underlying reasons customers are choosing to cancel their subscriptions.

### Task 5: Word Cloud Visualization
Generate word clouds for both full conversations and their summaries to visually identify common themes and customer concerns.

---

## ⚙️ Setup & Installation

### Prerequisites
- Python 3.12+
- Git
- VS Code (with Jupyter extension) or GitHub Codespaces

### Step 1: Clone the Repository
```bash
git clone https://github.com/your-username/genai-customer-insights-nlp.git
cd genai-customer-insights-nlp
```

### Step 2: Create and Activate Virtual Environment
```bash
# Create virtual environment
python -m venv venv

# Activate (Linux/Mac/Codespaces)
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install --upgrade pip
pip install transformers torch sentencepiece pandas numpy matplotlib seaborn scikit-learn jupyter ipykernel notebook tqdm datasets wordcloud
```

### Step 4: Register the venv as a Jupyter Kernel
```bash
python -m ipykernel install --user --name=venv --display-name "Python (venv)"
```

### Step 5: Generate requirements.txt
```bash
pip freeze > requirements.txt
```

### Step 6: Run the Notebook
Open `gen_ai_customer_insights.ipynb` in VS Code or Jupyter and select the **Python (venv)** kernel.

---

## 🔑 Key Findings

- **5 out of 20** conversations involved subscription cancellation requests
- Primary cancellation reasons: **delivery delays**, **poor ingredient quality**, **missing recipe cards**
- Most frequent issues: missing ingredients, damaged items, late deliveries
- Word cloud analysis reveals high frequency of terms: *delivery*, *cancel*, *ingredient*, *kit*, *issue*

---

## 📚 What You'll Learn

- **Generative AI (GenAI)** — How models like FLAN-T5 generate text from prompts
- **Natural Language Processing (NLP)** — Text classification, summarization, information extraction
- **AI Applications** — Real-world customer service analytics
- **Transformers Library** — Loading and using pre-trained models from Hugging Face

---

## 📝 Requirements

- Python Proficiency
- Basic Machine Learning Knowledge

---

## 🤝 Acknowledgements

- **Google** for the FLAN-T5 model
- **MoritzLaurer** for the multilingual zero-shot classification model
- **Hugging Face** for the Transformers library
- **Fresh Fare Meal Kits / QuickServe Meals** analytics team for the dataset and project brief

---

*Built with ❤️ for the QuickServe Meals Analytics Team*


