# 🎭 Sentiment Analysis of Movie Reviews

# 📌 Project Overview and Objectives
This project implements a **sentiment analysis system** for **IMDb movie reviews**, classifying them as **positive or negative**. The model is built using **Logistic Regression** and includes **text preprocessing, feature extraction, model training, evaluation, and deployment**. Additionally, we integrate **CodeCarbon** to track the environmental impact of training and **SHAP** for model explainability. The final model is optimized for **deployment on embedded systems like Arduino**.

# 📊 Dataset Download and Preprocessing
We use the **IMDb dataset** from Stanford, which contains **50,000** movie reviews labeled as **positive** or **negative**.

### **Download Dataset**
- 🔗 [Stanford IMDb Dataset](https://ai.stanford.edu/~amaas/data/sentiment/)

### **Preprocessing Steps**
1. Remove HTML tags, punctuation, and special characters.
2. Convert text to lowercase.
3. Remove stopwords.
4. Apply stemming and tokenization.
5. Transform text into TF-IDF feature vectors.

# 📈 Model Training and Evaluation
1. Load and preprocess the dataset.
2. Convert text to numerical representation using **TF-IDF**.
3. Train a **Logistic Regression model** on the processed data.
4. Evaluate performance using **accuracy, precision, recall, and F1-score**.
5. Use **SHAP** to explain how words influence predictions.

Example of classification report:
```
Precision  Recall  F1-score  Support
Positive      0.90    0.87      0.88    2500
Negative      0.87    0.90      0.89    2500
```

# 🌱 Carbon Footprint Analysis
We use **CodeCarbon** to measure the environmental impact of training our model. The emissions data is logged for analysis.

# 🔬 Ethical Considerations and Explainability
We use **SHAP (SHapley Additive exPlanations)** to visualize which words contribute the most to sentiment classification. 

Example SHAP summary plot:
```
great       → Positive
bad         → Negative
amazing     → Positive
boring      → Negative
```

We also discuss the fairness and accountability of using AI for sentiment analysis, considering potential biases in the model’s predictions.

# 🔧 Embedded System Deployment Insights
We convert the trained model for execution on **Arduino** by:
- Extracting weights & bias from the logistic regression model.
- Applying **quantization** to optimize performance.
- Generating a `.h` file for use in an **Arduino sketch**.

Example:
```cpp
#include "sentiment_model.h"
int predict_sentiment(int features[], int num_features) {
    int score = bias;
    for (int i = 0; i < num_features; i++) {
        score += weights[i] * features[i];
    }
    return score > 0 ? 1 : 0;
}
```


