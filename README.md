#  Detecting AI-Generated Product Reviews in Dravidian Languages

[![DOI](https://zenodo.org/badge/902793095.svg)](https://doi.org/10.5281/zenodo.14847233)

## 🚀 Introduction
The **Shared Task on Detecting AI-Generated Product Reviews in Dravidian Languages** focuses on addressing the rise of AI-generated product reviews in **Malayalam** and **Tamil**. As AI-generated content becomes more sophisticated, ensuring **authenticity in online reviews** is critical for consumer trust. 

This competition brings together **researchers and practitioners** to develop innovative models that can accurately distinguish AI-generated reviews from human-written ones. The datasets include both **AI-generated and human-authored reviews**, providing a real-world challenge for NLP experts.

## 🏅 Results in the Shared Task
| 🌍 Language  | 🏆 Rank | 📊 F1-Score |
|-------------|--------|------------|
| 🇮🇳 **Tamil**     | 🏆 **8**  | 🎯 **0.9298**   |
| 🇮🇳 **Malayalam** | 🏆 **11** | 🎯 **0.8797**   |

## 📌 Evaluation Criteria
✔️ Submissions were accepted **only through Google Forms**. *(Submission Closed)*  
✔️ Submission format: **team_name.zip** containing TSV files for each language as `teamname_language_run.tsv`  
&nbsp;&nbsp;&nbsp;&nbsp;✅ Example: `teamname_tamil_run.tsv`, `teamname_malayalam_run.tsv`  
✔️ **Macro Average F1-score** used for evaluation 📈  
✔️ **Classification system’s performance** measured in terms of **F1-Score** 🔍  

## 📂 Dataset & Task
Participants were challenged to build AI models capable of **differentiating between human-written and AI-generated reviews** for:
- 🇮🇳 **Tamil Product Reviews**
- 🇮🇳 **Malayalam Product Reviews**

### 📊 Dataset Classes
- **Human-Written Reviews**
- **AI-Generated Reviews**

## 🏆 Model Comparison & Performance Evaluation
| Model | 🇮🇳 Tamil Accuracy | 🇮🇳 Malayalam Accuracy |
|--------------|----------------|----------------|
| **BERT-Base-Multilingual-Cased** | 94% | 94% |
| **TF-IDF** | 81% | 76% |
| **Count Vectorizer** | 83% | 76% |
| **XLM-RoBERTa-Large** | 96% | 94% |

## 🧠 Models Used & Pretraining Methods
### **Models Used**
- **BERT-Base-Multilingual-Cased**
- **XLM-RoBERTa-Large**
- **TF-IDF with Logistic Regression**
- **Count Vectorizer with SVM**

### **Pretraining Methods**
- **BERT-Base-Multilingual-Cased:** Pretrained on 104 languages with masked language modeling.
- **XLM-RoBERTa-Large:** Trained on massive multilingual datasets with self-supervised learning.
- **TF-IDF & Count Vectorizer:** Statistical feature extraction techniques for text classification.

### 📌 **DOI Generation**
The code is archived and assigned a **DOI** through **Zenodo** for proper citation and reference.

## ✍️ Authors
- **Prethish GA** ([📧 Email](mailto:prethish0409@gmail.com))
- **Vasantharan K** ([📧 Email](mailto:vasantharank.work@gmail.com))

For further inquiries, feel free to reach out! 📩

