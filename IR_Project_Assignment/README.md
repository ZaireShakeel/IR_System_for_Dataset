# Information Retrieval – Assignment 3  
TF-IDF • BM25 • Hybrid Search • Evaluation

This project implements a full Information Retrieval pipeline using **TF-IDF**, **BM25**, and a **hybrid scoring model**.  
It supports query searching, ranking, and evaluation metrics like **Precision@5**, **Recall@5**, **F1@5**, **Average Precision**, and **Query Time**.

---

## 📂 Project Structure

```
/project-folder
│
├── Articles.csv
├── ir_project_assignment_3.py
└── README.md
```

---

## 📄 Description

The script performs the following:

1. **Loads Articles.csv**
2. **Cleans and preprocesses text**
3. **Converts documents into vectors using:**
   - TF-IDF
   - BM25
4. **Builds a Hybrid Search Model**
   - hybrid_score = α × TF-IDF_score + (1 − α) × BM25_score
5. **Runs multiple queries**
6. **Prints:**
   - Top-k ranked documents  
   - Precision@5  
   - Recall@5  
   - F1-score@5  
   - Average Precision (AP)  
   - Query Time

---

## 📦 Requirements

Install these dependencies before running the script:

```bash
pip install pandas numpy scikit-learn nltk rank-bm25
```

Additionally, the script will download required NLTK resources automatically (stopwords, punkt, etc.).

---

## ▶️ How to Run

1. Make sure `Articles.csv` and `ir_project_assignment_3.py` are in the same folder.
2. Open a terminal in that folder.
3. Run the script:

```bash
python ir_project_assignment_3.py
```

---

## ✔️ What happens when you run it?

The script will:
* Load and clean the dataset
* Compute TF-IDF vectors
* Build BM25 index
* Combine them for hybrid search
* Run queries (defined inside the script)
* Print:
   * Ranked results
   * Evaluation metrics
   * Processing time

---

## 🧪 Evaluation Metrics Explained

| Metric | Meaning |
|--------|---------|
| **Precision@5** | How many of the top 5 retrieved documents are relevant |
| **Recall@5** | How many of the relevant documents were found in the top 5 |
| **F1@5** | Harmonic mean of Precision@5 and Recall@5 |
| **AP (Average Precision)** | Measures how good the ranking is across all relevant documents |
| **Query Time** | How long the retrieval took |

---

## ⚙️ Configuration (Inside the Script)

You can adjust:
* The hybrid weight `alpha`
* Preprocessing steps
* The number of top results (k)

Example:

```python
ALPHA = 0.6
TOP_K = 5
```

---

## 📝 Notes

* Ensure the CSV file contains columns:
   * `ArticleId`
   * `ArticleTitle`
   * `ArticleContent`
* If your CSV has different column names, update them in the script.

---

## 📜 Author

This project was created for the course:

**Information Retrieval & Text Mining (IRTM)**  
**Assignment 3 – Search Models & Evaluation**

---

## 📄 License

This project is submitted as part of coursework for CS 516 at ITU.
