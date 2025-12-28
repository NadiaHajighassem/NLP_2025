# NLP-exam-2025-CogSci

Welcome! 👋  
This repository contains my project for the NLP exam in the Cognitive Science Master’s program at Aarhus University.

In this project, I collect data from two subreddits:

- `r/depression`
- `r/CasualConversation`

The goal is to explore **what BERT pays attention to in depressive vs. non-depressive text**.

**Due to ethical concerns, the datasets used in this project have not been uploaded to GitHub.**

---

## 🛠️ Repository Structure

```text
.
├── Scraping/
│   └── Scraping.ipynb    # Code for scraping subreddits
│ 
├── nbs/
│   ├── Finetune.ipynb    # Code for fine-tuning BERT
│   ├── Analysis.ipynb    # Code for attention probing
│   └── runs/             # Folder for fine-tuned models (not pushed due to size)
│   
├── requirements.txt      # Packages needed for running notebooks
└── README.md             # Info about the repo


---

## 🛠️ Setup (UCloud)

Before running any code, create a virtual environment and install the required packages.

From the project root:

```bash
# 1. Create virtual environment
python -m venv .venv

# 2. Activate it 
source .venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt

---

### ▶ Running the notebooks

The main results of this project are shown in the following notebooks:

1. `Scraping/Scraping.ipynb` – Data collection 
2. `nbs/Finetune.ipynb` – Fine-tuning BERT 
3. `nbs/Analysis.ipynb` – Attention analysis and results

⚠️ **Note:**  
- The scraping and fine-tuning steps are very time-consuming, so keep in mind, that some chunks take multiple hours to run (speficially fine-tuning)

# 4. Deactivate the environment when you're done
deactivate
