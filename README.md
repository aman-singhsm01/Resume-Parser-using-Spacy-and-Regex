# Resume-Parser-using-Spacy-and-Regex
An end-to-end Resume Parser built with spaCy NER and Regex that extracts structured information such as Name, Email, Phone, Skills, and Education from resumes. Trained on a Kaggle dataset and supports PDF upload with accurate parsing results.
## 📌 Project Description

This project is an **end-to-end Resume Parser** built using **Natural Language Processing (NLP)** techniques to automatically extract structured information from resumes. Instead of manually going through CVs, this system processes a **PDF resume** and extracts details such as **Name, Email, Phone Number, Skills, and Education** into a structured format (e.g., JSON).  

### 🛠️ Technologies Used
- **Programming Language**: Python 3.8+  
- **Libraries**: spaCy (NER model), Regex, PyMuPDF (PDF text extraction), Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- **Environment**: Google Colab / Jupyter Notebook  

### 📊 Dataset
The dataset is taken from **Kaggle**: [Entity Recognition in Resumes](https://www.kaggle.com/datasets/gauravduttakiit/entity-annotated-corpus).  
It contains annotated resumes in JSON/XML format with entity labels such as `Name`, `Email`, `Phone`, `Skills`, and `Education`. An extended dataset of ~5000 resumes was also used for training the model for better generalization.  

### 🔎 Algorithm & Approach
1. **Text Extraction**: Extract text from PDF resumes using PyMuPDF.  
2. **Preprocessing**: Clean text, normalize spacing, and prepare training data.  
3. **Custom NER Model**: Train a **spaCy Named Entity Recognition (NER)** model on Kaggle annotated resumes to identify entities.  
4. **Regex Enhancement**: Apply Regex rules for email and phone number detection, boosting accuracy.  
5. **Evaluation**: Use Precision, Recall, and F1-score to evaluate performance for each entity class.  
6. **Inference Pipeline**: Upload a resume → Extract text → Apply NER + Regex → Return structured JSON output.  

### 📈 Results
The model achieves **~92% overall accuracy**.  
- Best performing entities: **Email (98.5% F1-score)** and **Phone (96% F1-score)**  
- Strong results for Name, Skills, and Education with F1-scores above 85%.  

### 🚀 Conclusion
This Resume Parser demonstrates the power of combining **machine learning (NER)** with **rule-based Regex patterns** for robust information extraction. It is scalable, extendable to new entities like Work Experience and Projects, and can be deployed as a **web app** using Streamlit or Flask.  
