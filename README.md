# 🏢 Company Classifier – Insurance Taxonomy Mapping

![Python](https://img.shields.io/badge/Python-3.10-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Project-Finished-success)
![Updated](https://img.shields.io/badge/Last%20Updated-Mar%202024-orange)

## 📌 Project Overview
This project solves a real-world classification challenge: assigning companies to one or more relevant **insurance taxonomy labels** based on their business descriptions, tags, and industry metadata.

It was built as part of the **Veridion Machine Learning Challenge**, with scalability, interpretability, and efficiency in mind.

---

## 🧠 Objective
- Accept a list of companies with:
  - Description  
  - Business Tags  
  - Sector / Category / Niche  
- Accept a static taxonomy of insurance labels  
- Build a robust classifier that maps each company to one or more relevant insurance labels

---

## ⚙️ Approach

### ✅ Preprocessing
- Combined all relevant fields (description, tags, sector, category, niche)
- Cleaned and normalized all text

### ✅ Feature Engineering
- Used **TF-IDF vectorization** to represent company profiles and taxonomy labels
- Computed **cosine similarity** between companies and all insurance labels

### ✅ Classification
- Selected the **Top 3 most similar insurance labels** per company
- Annotated the company list with a new column: `insurance_label`

---

## 🛠️ Tools Used

- Python 3.10
- Pandas
- scikit-learn
- FPDF (for PDF export)
- Jupyter Notebook

---

## 📂 Project Structure

```
company_classifier_project/
├── classifier.ipynb                          # Main notebook with full code
├── README.md                                 # This file
├── data/
│   ├── ml_insurance_challenge.csv            # Input: company data
│   ├── insurance_taxonomy.xlsx               # Input: insurance taxonomy
│   └── annotated_company_list.csv            # Output: predictions
├── output/
│   └── classifier.ipynb                      # Copy of the notebook for output or presentation
├── Company-Classification-A-Machine-Learning-Approach.pdf   # Presentation (PDF)
├── Company-Classification-A-Machine-Learning-Approach.pptx  # Presentation (PPTX)
```

---

## 📈 Results
- TF-IDF performed well on industry-specific keywords (e.g. excavation, construction)
- Performance was weaker on generalized services or medical companies due to lack of semantic understanding
- Achieved fast and scalable classification with clear predictions

---

## 🔄 Future Improvements
- Use **Sentence-BERT** for semantic similarity
- Fine-tune a **multi-label classifier** on even small labeled datasets
- Apply **zero-shot learning** for rare/long-tail taxonomy labels
- Use **approximate similarity (e.g. Faiss)** for large-scale datasets

---

## ▶️ How to Run

1. Clone this repository  
2. Place your input files in the `data/` folder  
3. Open and run `insurance_classifier.ipynb`  
4. View the predictions in `annotated_company_list.csv`

---

## 🏁 Submission
This project was created as part of the **Veridion ML Challenge**.  
If you'd like to collaborate or give feedback, feel free to open an issue or connect!

---

## 👤 Author

**Stefan Alexandru**  
Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/stefan-alexandru-funariu/) or check out more projects at [GitHub](https://github.com/StefanAlexandruFunariu)

---

> Made with 💡 and a lot of `cosine_similarity()`
