# 🚀 Intelligent Resume Ranking Engine

<div align="center">

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/NLP-TF--IDF-blueviolet?style=for-the-badge" alt="TF-IDF" />
<img src="https://img.shields.io/badge/Similarity-Cosine-green?style=for-the-badge" alt="Cosine Similarity" />
<img src="https://img.shields.io/badge/CSV-Data%20Processing-orange?style=for-the-badge" alt="CSV Processing" />

</div>

<br />

A lightweight yet powerful **Resume Ranking Engine** built entirely in **pure Python**, designed to intelligently match candidates against multiple Job Descriptions (JDs) using:

- **Skill Normalization**
- **TF-IDF Vectorization**
- **Cosine Similarity**
- **Alias-based NLP preprocessing**

The system automatically processes resumes, standardizes inconsistent skill names, computes relevance scores, and ranks the most suitable candidates for each role.

---

# ✨ Features

- 🧠 **Custom Skill Normalization Engine**
  - Handles spelling mistakes, aliases, abbreviations, and formatting inconsistencies.
  - Example:
    ```text
    Pyhton → python
    MachineLearning → machine_learning
    Reactjs → react
    kubernates → kubernetes
    ```

- 📊 **Pure Python TF-IDF Implementation**
  - No Scikit-learn.
  - No external ML libraries.
  - Entire vectorization pipeline implemented manually.

- ⚡ **Cosine Similarity-Based Ranking**
  - Computes semantic proximity between Job Descriptions and candidate profiles.

- 📁 **CSV-Based Candidate & Job Processing**
  - Reads structured datasets directly from CSV files.

- 🔍 **Dynamic Vocabulary Generation**
  - Builds vocabulary automatically from normalized candidate skill corpus.

- 🧮 **Document Frequency & IDF Calculation**
  - Penalizes overly common skills while rewarding specialized expertise.

- 🧹 **Deduplication & Cleaning**
  - Removes duplicate skills while preserving order.

- 🏆 **Top Candidate Recommendation System**
  - Returns top-ranked candidates for every job posting.

---

# 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Programming Language | Python 3 |
| Data Handling | CSV Module |
| NLP Logic | Pure Python |
| Similarity Engine | TF-IDF + Cosine Similarity |
| Mathematical Computation | math module |
| Skill Processing | Regex + Alias Mapping |

---

# 🧠 How the Engine Works

## 1️⃣ Skill Normalization

Raw candidate skills are standardized using a comprehensive alias dictionary.

Example:

```text
"Pyhton, MachineLearning, Deep-learning"
```

becomes:

```text
["python", "machine_learning", "deep_learning"]
```

---

## 2️⃣ Vocabulary Construction

A global vocabulary is generated dynamically from all normalized candidate skills.

Example:

```text
[
 python,
 machine_learning,
 tensorflow,
 react,
 docker
]
```

---

## 3️⃣ TF-IDF Vectorization

Each candidate resume is transformed into a weighted vector representation.

### Term Frequency (TF)

TF(t,d)=1 / Total Unique Skills in Resume

### Inverse Document Frequency (IDF)

IDF(t)=ln(N / DF(t))

Where:

- N = Total number of resumes
- DF(t) = Number of resumes containing skill t

---

## 4️⃣ Job Description Vectorization

Each Job Description is converted into a binary vector indicating required/preferred skills.

Example:

```text
{
 python: 1,
 tensorflow: 1,
 react: 0
}
```

---

## 5️⃣ Cosine Similarity Matching

Candidate TF-IDF vectors are compared against Job Description vectors using cosine similarity.

cos(θ)=(A·B)/(|A||B|)

Higher similarity score → better candidate-job alignment.

---

# 📂 Project Structure

```bash
resume-ranking-engine/
│
├── jobs.csv
├── candidates.csv
├── main.py
├── README.md
```

---

# 🚀 Getting Started

## Prerequisites

Make sure Python 3 is installed:

```bash
python --version
```

---

# ⚙️ Installation

## Clone the Repository

```bash
git clone https://github.com/your-username/resume-ranking-engine.git
cd resume-ranking-engine
```

---

# ▶️ Run the Project

```bash
python main.py
```

---

# 📊 Example Output

```text
JD-1 — Kakao (ML Engineer)
Sneha Patel(0.57), Karan Mehta(0.53), Arjun Sharma(0.40)

JD-2 — Naver (Backend Engineer)
Rahul Gupta(0.81), Ananya Krishnan(0.28), Deepika Rao(0.19)

JD-3 — Line (Frontend Engineer)
Aditya Kumar(0.67), Priya Nair(0.58), Ananya Krishnan(0.35)
```

---

# 📈 Supported Skill Domains

The engine currently supports normalization across:

- Programming Languages
- Machine Learning
- Deep Learning
- NLP
- Frontend Development
- Backend Development
- Databases
- DevOps & Cloud
- Mobile Development
- Data Visualization
- CS Fundamentals
- UI/UX Tools

---

# 🔬 Core Algorithms Implemented

- Skill Alias Normalization
- Vocabulary Generation
- Document Frequency Computation
- Inverse Document Frequency (IDF)
- TF-IDF Vector Construction
- Binary JD Vector Construction
- Cosine Similarity Matching
- Candidate Ranking System

---

# 🎯 Key Highlights

✅ No external machine learning libraries  
✅ Fully explainable ranking system  
✅ Handles spelling errors and aliases  
✅ Efficient lightweight implementation  
✅ Easily extensible skill ontology  
✅ Beginner-friendly NLP architecture  
✅ Strong foundation for ATS systems  

---

# 🚧 Future Improvements

Potential future upgrades:

- Sentence Embeddings (BERT / SBERT)
- Semantic Skill Matching
- Resume PDF Parsing
- Experience Weighting
- Recruiter Dashboard UI
- Hybrid BM25 + Embedding Search
- Vector Database Integration
- Multi-Agent Recruitment AI System

---

# 📄 License

This project is open-sourced under the MIT License.

---

<div align="center">

### <i>Built for intelligent candidate ranking, scalable resume analysis, and explainable AI-driven hiring systems.</i>

</div>
