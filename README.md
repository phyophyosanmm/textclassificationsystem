## 📈 Final Results – Text Classification (Spam Detection)

### 🔍 Overview
Part B focused on building a supervised machine learning pipeline to classify SMS messages as **ham (genuine)** or **spam**. The dataset contained 5,572 messages, with a highly imbalanced distribution (86.6% ham, 13.4% spam). Preprocessing included label encoding, stratified train-test split, and feature engineering using **CountVectorizer** and **TF-IDF** with unigrams and bigrams.

---

### 📊 Performance
| Model                  | Accuracy | Precision | Recall | F1-Score | Notes |
|-------------------------|----------|-----------|--------|----------|-------|
| Multinomial Naïve Bayes | ~96%     | 0.95      | 0.94   | 0.95     | Strong baseline, effective with TF-IDF features |
| Logistic Regression     | ~97%     | 0.96      | 0.95   | 0.96     | Balanced precision and recall, suitable for real-time deployment |
| Support Vector Machine  | **98%**  | 0.97      | 0.97   | 0.97     | Best overall performance, robust decision boundaries |

---

### 📝 Key Insights
- **Naïve Bayes** provided a fast and effective baseline, especially with TF-IDF features.  
- **Logistic Regression** achieved balanced results, making it practical for real-time spam filtering.  
- **SVM** delivered the highest accuracy and robustness, outperforming other models in handling imbalanced data.  
- **EDA findings** showed spam messages tend to be longer and use promotional language (e.g., “free”, “win”, “call”), while ham messages are conversational (e.g., “love”, “time”, “meet”).  

---

### ⚠️ Limitations
- Dataset imbalance (ham >> spam) required careful evaluation using precision, recall, and F1-score.  
- Deep learning models were not explored extensively due to dataset size and computational constraints.  

---

### ✅ Conclusion
Classical machine learning models, particularly **SVM with TF-IDF features**, proved most effective for SMS spam detection. The pipeline demonstrated strong accuracy, robustness, and practical applicability for real-world spam filtering systems.
