# 🤖 GenAI

A collection of projects exploring Large Language Models (LLMs), AI Agents, and NLP techniques — from simple Q&A apps to emotion classification systems.

This repository grows over time as I learn and build more in the AI space.

---

## 📁 Projects

| # | Project | Description | Tools |
|---|---------|-------------|-------|
| 01 | [PDF Q&A Bot](./01-PDF-Q&A-bot/) | Ask questions about PDF documents using open-source LLMs | Gradio, Llama, HuggingFace |
| 02 | [Emotion Classification with DistilBERT](./02-Emotion-Classification-DistilBERT/) | Detect emotions from text using a fine-tuned DistilBERT model | Python, Transformers, HuggingFace |
| ... | *More coming soon* | | |
---

## 🧠 What is an LLM?

A **Large Language Model (LLM)** is an AI model trained on massive amounts of text that can understand and generate human language. Examples include Llama, Mistral, GPT, and Gemini.

---

## 🛠️ Tech Stack Used Across Projects

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Gradio | Building web UIs |
| HuggingFace | Models and deployment |
| Transformers | Fine-tuning and inference |
| LangChain | Building LLM pipelines and agents |
| pypdf | PDF processing |
| PyTorch | Deep learning framework |
| Google Colab | Development and experimentation |

---

## 🗺️ Roadmap

- ✅ PDF Q&A Bot
- ✅ Emotion Classification with DistilBERT

---

# 📊 Startup Expansion Analysis

This project analyzes store expansion and performance across different states using **Python** (pandas, numpy, matplotlib, seaborn) for data preprocessing, and **Power BI** for interactive dashboard visualization.

---

## 🚀 Project Workflow

### 1. Data Import & Cleaning (Python)

- Loaded the raw dataset.
- Handled missing values and inconsistencies.
- Renamed and formatted columns.
- Applied feature engineering (e.g., `Performance_State`, deviation %, below-target flag).

### 2. Preprocessing & Processing (Python)

**Statistical checks for outliers:**

- Used the standard deviation method to detect anomalies.
- Plotted histograms to visually confirm the data distribution and validate that there are no major outliers.

**New derived metrics:**

- Profit deviation percentage
- Performance categories
- Losing store indicator

**Export:** saved a cleaned dataset for visualization.

### 3. Dashboard Creation (Power BI)

Designed an interactive dashboard to explore:

- Store distribution by state
- Profit contribution by region
- Store performance segmentation
- Impact of marketing spend

---

## 📈 Dashboard Preview

The dashboard highlights:

- **KPIs:** Total Profit, Marketing Spend, Number of States, Number of Stores
- **Pie Chart:** Distribution of store performance states
- **Bar Charts:** Profit contribution by state, and performance split between losing and winning stores

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python** (pandas, numpy, matplotlib, seaborn) | Data cleaning & processing |
| **Power BI** | Dashboard & visualization |

---

## 🔮 Insights & Findings

- ✅ **California** has the highest store count and profit contribution, but also a notable number of losing stores.
- ✅ Performance distribution shows a significant percentage of stores falling into "Very Poor" (-25%+).
- ✅ Marketing spend alone does not guarantee profit; performance varies significantly by state.
- ✅ The data quality check confirmed no major outliers, ensuring reliable performance insights.

---

## 📌 Next Steps

- Incorporate time-series trends (profit over time).
- Add predictive modeling for store success probability.
- Enhance geospatial visualization for store expansion planning.

---

## 📄 License

This portfolio is released under the MIT License — feel free to use it for
learning or as a portfolio reference.

---

## 👨‍💻 Author

**Sara Ibrahim**  
*Data Scientist | Machine Learning / AI Engineer*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/sara-ibrahim-omran)  
[![Email](https://img.shields.io/badge/Email-Contact%20Me-red?style=flat&logo=gmail)](mailto:Saraomran433@gmail.com)

### 🌟 Let's Connect!

I'm passionate about solving real-world problems with data, machine learning, and AI. Feel free to reach out for:

- 💼 Job opportunities and collaborations
- 📚 Technical discussions and knowledge sharing
- 🚀 Project ideas and innovative solutions

**⭐ If you find this project helpful, please give the repo a star!**

---

## 📄 License

This repository is open source and available under the [MIT License](LICENSE).
