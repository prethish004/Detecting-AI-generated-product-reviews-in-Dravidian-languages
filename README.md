# Detecting-AI-generated-product-reviews-in-Dravidian-languages
![image](https://github.com/user-attachments/assets/3f55e85b-f106-4def-87a4-91cf36a4c0ba)

The "Shared Task on Detecting AI-generated Product Reviews in Dravidian Languages" aimed at addressing the growing concern of AI-generated product reviews, specifically in Dravidian languages, specifically in Malayalam and Tamil. As AI tools become more advanced, the ability to distinguish between human-written and AI-generated content has become increasingly crucial, especially in the domain of online reviews where authenticity is essential for consumer decision-making. This shared task brings together researchers and practitioners to develop and evaluate models that can accurately identify AI-generated reviews in these languages. Participants will work with datasets consisting of both human-written and AI-generated reviews, and the task will explore challenges unique to Dravidian languages.
# Team Name :The_Deathly_Hallows
## Model Performance

| Language  | Rank | F1-Score |
|-----------|------|----------|
| **Tamil**      | 🏆8    | **0.9298**  |
| **Malayalam**  | 🏆11   | **0.8797**  |

🎯 The model demonstrates high accuracy in both Tamil and Malayalam language tasks, achieving impressive F1-scores!

# Model Workflow

<p align="center">
  <img src="https://github.com/user-attachments/assets/9c04504f-dafd-45d5-9a18-4a886803f5b9" alt="Untitled Diagram-Page-1">
</p>

---

# 📝 AI vs Human: Dravidian Language Review Classification  

## 📌 Dataset Description  

The dataset consists of **AI-generated** and **human-written** product reviews in **Malayalam** and **Tamil**. It was designed to help build models that differentiate between machine-generated and human-authored reviews.  

### 🔹 Dataset Distribution  

| Language   | AI-Generated Reviews | Human-Written Reviews | Total Samples |
|------------|----------------------|----------------------|--------------|
| **Tamil**      | 405                  | 403                  | 808          |
| **Malayalam**  | 400                  | 400                  | 800          |

📌 *Balanced datasets ensure fair evaluation of classification models.*  

---

## 🛠 Methodology  

### 📌 1️⃣ Preprocessing  
Each dataset entry includes:  
✔️ A unique **ID**  
✔️ A **textual review (transcript)**  
✔️ A **class label** (AI-generated or human-written)  

📌 **Preprocessing Steps:**  
- ✅ **Tokenization**: Used the corresponding transformer model tokenizer.  
- ✅ **Stopword Removal**:  
  - Malayalam stopwords were obtained from a public repository.  
  - Tamil stopwords were removed using **Advertools**.  
- ✅ **Text Normalization**:  
  - **Tamil**: Processed using **Indic NLP Library**.  
  - **Malayalam**: Tokenized using the **indic-tokenize** package.  

---

### 📌 2️⃣ Feature Extraction  
Three methods were used to extract meaningful text features:  

🔹 **TF-IDF**: Converts text into numerical vectors based on word importance.  
🔹 **Count Vectorizer**: Represents word occurrences as sparse matrices.  
🔹 **Transformer-Based Embeddings**:  
   - **BERT-Base-Multilingual-Cased**  
   - **XLM-RoBERTa-Large**  
   📌 Extracted contextual embeddings using the **mean of the last hidden state outputs**.  

---

### 📌 3️⃣ Classification Model  

A deep-learning-based classification model was developed with the following architecture:  

🔹 **Input Layer**: Tokenized text input.  
🔹 **Hidden Layers**:  
   - Fully connected **Dense layer** with **256 neurons** & ReLU activation.  
   - **Batch normalization** & **Dropout (0.5)** to prevent overfitting.  
   - Another **Dense layer** with **128 neurons** & ReLU activation, followed by batch normalization & dropout.  
🔹 **Output Layer**:  
   - Softmax activation for final classification.  

📌 **Training Details:**  
✔️ **Optimizer**: Adam  
✔️ **Loss Function**: Categorical Cross-Entropy  
✔️ **Data Split**: **80% training** | **20% testing** using `train_test_split` from Scikit-learn.  

---


## 🏆 Model Performance Comparison

| 🏷️ Models Used                  | 🇮🇳 Tamil Accuracy | 🇮🇳 Malayalam Accuracy |
|----------------------------------|------------------|----------------------|
| **BERT-Base-Multilingual-Cased** | 🟢94%             | 🟢94%                 |
| **TF-IDF**                       | 🟡81%             | 🔴76%                 |
| **Count Vectorizer**             | 🟡83%             | 🔴76%                 |
| **XLM-RoBERTa-Large**            | **96%** 🔥      | **94%** 🔥          |

### 🔍 Key Observations:
- 🚀 **XLM-RoBERTa-Large** achieves the highest accuracy for both Tamil (**96%**) and Malayalam (**94%**).
- 🤖 **BERT-Base-Multilingual-Cased** also performs well with **94%** in both languages.
- 📊 **TF-IDF** and **Count Vectorizer** show lower performance, indicating that deep learning models are more effective for this task.

---

💡 *For best results, XLM-RoBERTa-Large is recommended for Tamil and Malayalam NLP tasks.*



