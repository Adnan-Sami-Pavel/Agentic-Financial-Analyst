# Agentic-Financial-Analyst
A multi-agent AI system using CrewAI and heterogeneous LLMs for advanced financial sentiment analysis and reporting.
# 🤖 Agentic Financial Analysis: A Multi-Agent Framework for Nuanced Sentiment Analysis

![Language](https://img.shields.io/badge/Python-3.10%2B-blue)
![Framework](https://img.shields.io/badge/Framework-CrewAI-orange)
![LLM Provider](https://img.shields.io/badge/LLM-Groq%20(Llama%203.1)-green)

This repository contains the code for my research project on using a heterogeneous multi-agent system to achieve a more accurate and nuanced understanding of financial sentiment in text.

---
## 📖 Project Overview

Traditional sentiment analysis often fails with complex financial texts that contain speculation, sarcasm, or comparative language. This project tackles that problem by moving beyond a single AI model and instead creating a **"committee of expert agents,"** each with a unique specialization.

These agents analyze a piece of text from their own distinct perspective. A final "Synthesizer" agent then reviews their reports, weighs their confidence, and makes a final, reasoned judgment on the overall sentiment. This approach mimics a real-world financial analysis team and has shown promising results in classifying complex statements.

This project is the practical implementation of the framework proposed in my research paper, **"Structured Prompting and Heterogeneous LLM Multi-Agent Framework for Financial Sentiment Analysis,"** which was submitted to the IEEE COMPAS 2025 conference. 

---
## ✨ Key Features

* **Multi-Agent System:** Utilizes a team of **seven specialized AI agents** built with **CrewAI**.
* **Diverse Expert Personas:** Includes agents specializing in linguistics, rhetoric, comparative logic, institutional investing, and retail trading to capture different layers of meaning.
* **High-Speed Inference:** Powered by **Groq** using the Llama 3.1 model for near-instantaneous analysis.
* **Structured Output:** The final agent produces a detailed JSON object with the sentiment, confidence score, and a clear justification for its decision.
* **Performance Evaluation:** The system's accuracy and F1-score are benchmarked against a ground-truth dataset using Scikit-learn.

---
## 🏛️ Project Architecture

The system processes each piece of financial text through a sequential pipeline of specialist agents. Each specialist produces a high-level analysis, which is then passed to a final agent for synthesis.


---
## 🛠️ Technologies Used

* **Primary Framework:** [CrewAI](https://www.crewai.com/)
* **LLM Integration:** `langchain-groq`
* **Core Libraries:** `pandas`, `scikit-learn`
* **Development Environment:** Python 3.11, Google Colab

---
## 🚀 Setup and Usage

To get this project running locally, follow these steps.

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YourUsername/agentic-financial-analyst.git](https://github.com/YourUsername/agentic-financial-analyst.git)
    cd agentic-financial-analyst
    ```

2.  **Set Up a Virtual Environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Configure API Keys:**
    Create a `.env` file in the root directory and add your Groq API key:
    ```
    GROQ_API_KEY="your-groq-api-key-here"
    ```

5.  **Run the Analysis:**
    Execute the main notebook or a Python script to begin the analysis on the provided dataset.

