# NLP-exam-2025-CogSci

Welcome! 👋  
This repository contains my project for the NLP exam in the Cognitive Science Master’s program at Aarhus University.

In this project, I collect data from two subreddits:

- `r/depression`
- `r/CasualConversation`
  
The goal of this project is to assess whether linguistic markers of depression can also be identified by a transformer model trained to classify Reddit text as either depressive or non-depressive.

**Due to ethical concerns, the datasets used in this project have NOT been uploaded to GitHub. For examination the dataset has been uploaded to WiseFlow**

---

## 🛠️ Repository Structure

```text
.
├── Scraping/
│   └── Scraping.ipynb    # Code for scraping subreddits
│ 
├── data/
│    └── reddit_probe_triplets_20_pronounvar.csv # probing sentences
│ 
├── nbs/
│   ├── Finetune.ipynb    # Code for fine-tuning BERT
│   ├── Analysis.ipynb    # Code for attention probing
│   └── runs/             # Folder for fine-tuned models (not pushed due to size)
│ 
├── results/
│    └── figures/ # This folder contains figures of the results produced from attention probing
│ 
├── requirements.txt      # Packages needed for running notebooks
└── README.md             # Info about the repo

```

## 🛠️ Setup (UCloud)

Most of the code was executed locally on a MacBook 14" (2024, 16GB), while model fine-tuning was performed on UCloud using Coder Python 1.105.0 with GPUs."

Before running any code, create a virtual environment and install the required packages.

From the project root:

```bash
# 1. Create virtual environment
python -m venv .venv

# 2. Activate it 
source .venv/bin/activate

# 3. Install the requires packages
pip install -r requirements.txt

---

### ▶ Running the notebooks

The main results of this project are shown in the following notebooks:

1. `Scraping/Scraping.ipynb` – Data collection 
2. `nbs/Finetune.ipynb` – Fine-tuning BERT 
3. `nbs/Analysis.ipynb` – Attention analysis and results

To run any script in the Scraping or nbs folders, follow these steps with the virtual environment activated:

# For data scraping:
jupyter notebook Scraping/Scraping.ipynb

# For fine-tuning BERT:
jupyter notebook nbs/Finetune.ipynb

# For attention analysis:
jupyter notebook nbs/Analysis.ipynb


⚠️ **Note:**  
- The scraping and fine-tuning steps are very time-consuming, so keep in mind, that some chunks take multiple hours to run.

# Deactivate the environment when you're done
deactivate
