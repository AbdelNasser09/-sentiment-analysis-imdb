# -sentiment-analysis-imdb
Sentiment analysis system for IMDb movie reviews using Logistic Regression.   Includes text preprocessing, TF-IDF feature extraction, model training, evaluation (precision, recall, F1-score), and explainability with SHAP.   Optimized for deployment on embedded systems like Arduino.  
🎭 Sentiment Analysis of Movie Reviews

# -📌 Project Overview

This project implements a sentiment analysis system for IMDb movie reviews, classifying them as positive or negative. The model is built using Logistic Regression and includes text preprocessing, feature extraction, model training, evaluation, and deployment. Additionally, we integrate CodeCarbon to track the environmental impact of training and SHAP for model explainability.

# -👥 Team Members

Abdoul Nasser Adamou Soumana

Oumar Kone

# -🏆 Features Implemented

✅ IMDb dataset preprocessing (text cleaning, tokenization, stopword removal)

✅ TF-IDF feature extraction

✅ Logistic Regression model training

✅ Model evaluation (Confusion Matrix, Precision, Recall, F1-score)

✅ Carbon footprint analysis with CodeCarbon

✅ Explainability using SHAP

✅ Deployment on embedded systems (Arduino, .h file generation)

📂 Project Structure

📦 sentiment-analysis-imdb
 ├── 📁 data               # IMDb dataset files
 ├── 📁 models             # Trained models and weights
 ├── 📁 scripts            # Python scripts for preprocessing, training, evaluation
 ├── 📁 deployment         # Arduino `.h` file and embedded model conversion
 ├── 📄 README.md          # Project documentation
 ├── 📄 requirements.txt   # Required dependencies
 ├── 📄 main.py            # Main execution file

📊 Dataset

We use the IMDb dataset from Stanford, which contains 50,000 movie reviews labeled as positive or negative.

🔗 Download Dataset

🚀 Installation & Setup

1️⃣ Clone the Repository

git clone https://github.com/your-username/sentiment-analysis-imdb.git
cd sentiment-analysis-imdb

2️⃣ Install Dependencies

pip install -r requirements.txt

3️⃣ Run the Model

python main.py

📈 Model Training

Load and preprocess the dataset.

Convert text to numerical representation using TF-IDF.

Train a Logistic Regression model on the processed data.

Evaluate performance using accuracy, precision, recall, and F1-score.

Use SHAP to explain how words influence predictions.

🔍 Model Evaluation

Example of classification report:

Precision  Recall  F1-score  Support
Positive      0.90    0.87      0.88    2500
Negative      0.87    0.90      0.89    2500

🌱 Carbon Footprint Tracking

We use CodeCarbon to measure the environmental impact of training our model. The emissions data is logged for analysis.

🔬 Explainability with SHAP

We use SHAP (SHapley Additive exPlanations) to visualize which words contribute the most to sentiment classification.
Example SHAP summary plot:

great       → Positive
bad         → Negative
amazing     → Positive
boring      → Negative

🔧 Deployment on Embedded Systems (Arduino)

We convert the trained model for execution on Arduino by:

Extracting weights & bias from the logistic regression model.

Applying quantization to optimize performance.

Generating a .h file for use in an Arduino sketch.

📜 License

This project is released under the MIT License.

🛠 Future Improvements

Fine-tune model hyperparameters.

Experiment with deep learning alternatives (LSTM, Transformer models).

Optimize embedded model execution for low-power devices.

💡 Acknowledgments

Special thanks to Stanford AI Lab for the IMDb dataset.

🚀 Developed by Abdoul Nasser Adamou Soumana & Oumar Kone 🚀

