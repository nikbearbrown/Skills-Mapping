# Skills Mapping


## Overview

**AI4ED Lex** is an open-source **lexical database** designed for **skills mapping** in job-related texts such as **job descriptions and educational materials**. It applies **natural language processing (NLP)** techniques, **Poisson distribution**, and **semantic relations** to classify and enrich employment-related terminology.

This project aims to enhance **skills mapping** by:
- Organizing job-related terminology into **semantic sets**.
- Mapping terms to **synonyms, acronyms, spelling variants, and job classifications**.
- Using **LLMs, statistical methods, and NLP tools** to improve accuracy.

## Key Features

 **Discriminating Terms**: Identifies employment-related terms using Poisson distribution.  
 **Semantic Enrichment**: Utilizes **NLTK, spaCy, and PyDictionary** for enhanced tagging.  
 **Acronym Detection**: Implements custom heuristics for **recognizing industry-specific acronyms**.  
 **Contextual Rolling Window Classification (CRWC)**: Tags job descriptions by analyzing contextual words.  
 **LLM Integration**: Uses **AI models to verify and enrich missing data**.   
 **Comparison with Existing Frameworks**: Evaluates AI4ED Lex against **WGU Skills Library, ESCO, O*NET, and commercial tools**.  

---

## 📂 Project Structure


AI4ED-Lex-Skills-Mapping/
│── README.md              # Project overview and setup instructions     
│── docs/                  # Documentation files     
│   ├── methodology.md     
│   ├── evaluation.md     
│   ├── comparison.md     
│── data/                  # Sample datasets    
│── scripts/               # Python scripts for processing    
│   ├── tag_extraction.py    
│   ├── acronym_detection.py    
│   ├── skill_mapping.py     
│── models/                # Pre-trained models      
│── results/               # Output files, analysis results     
│── LICENSE                # License for open-source use    
│── .gitignore             # Files to ignore in GitHub commits    
│── requirements.txt       # Dependencies for running the project     



## 📜 Methodology

### **Discriminating Terms Extraction**
- Uses **Poisson distribution** to identify key job-related terms.
- Formula:  
  \[
  p(n | N, f) = e^{-Nf} \cdot \frac{(Nf)^n}{n!}
  \]

### **Semantic Enrichment**
- **Synonyms, acronyms, spelling variants, hypernyms, and meronyms** mapped using:
  - **NLTK + WordNet**
  - **spaCy NLP processing**
  - **PyDictionary for definitions**

### **Acronym Detection Heuristics**
- **Four custom heuristics** for industry-specific acronyms:
  1. **Classic Acronym Test** (e.g., "PMP" for Project Management Professional).
  2. **Skip-a-Word Acronym Test** (e.g., "CRISC" for Certified in Risk and Information Systems Control).
  3. **Substitution Acronym Test** (e.g., "CWNA" for Certified Wireless Network Administrator).
  4. **Composite Acronym Test** (e.g., "PharmD" for Doctor of Pharmacy).

### **Contextual Rolling Window Classification (CRWC)**
- Applies a **rolling 50-word window** to classify job-related terms into:
  - Certification
  - Language
  - Job Title
  - Sector
  - Skill
  - Trait

### **LLM Enrichment**
- **Uses API-integrated Large Language Models (LLMs)** to:
  - Fill missing **definitions** and classifications.
  - Validate **synonyms and semantic relations**.

---

## 📊 Evaluation & Benchmarking

### **Comparison with Existing Frameworks**
| Framework | Strengths | Limitations |
|-----------|-----------|-------------|
| **ESCO** | Multilingual job classification | Limited text mining capabilities |
| **O*NET** | Comprehensive job characteristics | Lacks NLP integration |
| **SFIA** | IT skills framework | Not generalized beyond IT |
| **WGU Skills Library** | Well-structured educational ontology | Not designed for free-text NLP |

### **Comparison with Commercial Skill Mapping Tools**
- Evaluates **AI4ED Lex vs. LightCast, Burning Glass, etc.**
- **Findings**: AI4ED Lex **matches or exceeds recall in identifying job-specific skills**.

---

## 🚀 Getting Started

### **Installation**
Clone the repository and install dependencies:
```bash
git clone https://github.com/your-username/AI4ED-Lex-Skills-Mapping.git
cd AI4ED-Lex-Skills-Mapping
pip install -r requirements.txt




