# 🎬 IMDb Movie Review Sentiment Analysis (NLP)

This project builds a **binary text classification model** to predict whether an IMDb movie review is **positive** or **negative** using Natural Language Processing (NLP) and machine learning.

---

## 🎯 Objective

Develop a machine learning model that can accurately classify IMDb movie reviews into:

- **Positive**
- **Negative**

using only the **text of the review**.

---

## 🗂️ Dataset

- **Source:** IMDb movie reviews dataset (`Imdb`)
- **Records:** ~50,000 reviews (edit this if your number is different)
- **Target variable:** `sentiment` → `positive` / `negative`

**Main columns:**

- `review` – raw text of the movie review  
- `sentiment` – label for each review (`positive` or `negative`)

---

## 🛠 Tech Stack

- **Language:** Python  
- **Environment:** Jupyter Notebook  

**Libraries:**

- Data handling: `pandas`, `numpy`
- NLP & preprocessing: `nltk`, `re`, `string`
- Machine learning: `scikit-learn`
- Visualization: `matplotlib`, `seaborn`

---

## 🔄 Project Workflow

### 1️⃣ Exploratory Data Analysis (EDA)

- Checked dataset shape, data types, and basic statistics  
- Verified presence of **missing values**  
- Analyzed **class balance** between positive and negative reviews  
- Examined:
  - Distribution of review lengths (word count / character count)
  - Sample reviews from each sentiment class

---

### 2️⃣ Text Preprocessing

Preprocessing steps applied to the `review` text:

- Lowercasing all text  
- Removing:
  - HTML tags  
  - Punctuation  
  - Numbers  
  - Special characters  
- Tokenization (splitting text into words)  
- Stopword removal using **NLTK**  
- Lemmatization / stemming to normalize words (e.g., “running” → “run”)  

These steps converted raw text into clean, normalized tokens ready for feature extraction.

---

### 3️⃣ Feature Engineering

Converted text data into numerical form using:

- **Bag-of-Words**
- **TF-IDF (Term Frequency–Inverse Document Frequency)**  
  - Uni-grams and bi-grams tested

Additional textual features (if used):

- Review length (number of words)  
- Character count  
- Average word length  

The final model primarily uses **TF-IDF vectors** as features.

---

### 4️⃣ Model Development

Trained and compared multiple classification algorithms:

- Logistic Regression  
- Multinomial Naive Bayes  
- Support Vector Machine (SVM)  
- Random Forest  

Steps followed:

- Train–test split (e.g., 80% train, 20% test)  
- Feature scaling where required  
- Hyperparameter tuning using **GridSearchCV / cross-validation** (on selected models)

---

### 5️⃣ Model Evaluation

Evaluated models using standard classification metrics:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- Confusion matrix to inspect misclassifications

Visualizations included:

- Confusion matrix heatmap  
- Comparison of model scores  
- Distribution of predicted vs actual labels  

---

## 📊 Example Results (Replace with Your Actual Metrics)

> 🔥 These are placeholder numbers. Update them from your notebook.

- **Best model:** Logistic Regression with TF-IDF features  
- **Test accuracy:** ~**90–92%**  
- **F1-score:** ~**0.90**  

**Insights:**

- Positive reviews often contained words like:  
  `excellent`, `amazing`, `brilliant`, `wonderful`, `masterpiece`  

- Negative reviews frequently used:  
  `boring`, `waste`, `worst`, `terrible`, `disappointing`  

- Very short reviews tended to be noisy and harder to classify correctly.

---

## 📁 Files in This Repository

- `NLPProject1.ipynb` – main Jupyter Notebook containing:
  - EDA  
  - Text preprocessing  
  - Feature engineering  
  - Model training & evaluation  

- `data_imdb_sample.csv` (optional) – a small sample of the IMDb dataset for demonstration


---


