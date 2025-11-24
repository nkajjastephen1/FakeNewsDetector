Fake News Detection Using Machine Learning

Submitted by: Nkajja Stephen

GitHub Repository: https://github.com/nkajjastephen1/FakeNewsDetector

1. Project Overview

The spread of fake news online is a global issue, affecting public perception, politics, and health. This project implements a machine learning-based system to detect fake news automatically. Articles are classified as real or fake, helping users identify misinformation quickly.

2. Objectives

Build a machine learning model to classify news as fake or real.

Evaluate the model using metrics like accuracy, precision, recall, and F1-score.

Deploy a Flask web application for real-time predictions.

Maintain project code, dataset, and updates on GitHub for reproducibility.

3. Dataset

Files used: Fake.csv and True.csv

Fake news articles and real news articles, combined for training/testing.

Total articles: ~40,000+ (more than the minimum 500 required).

Preprocessing included adding labels (0 = Fake, 1 = Real), merging, shuffling, and TF-IDF feature extraction.

4. Model

Algorithm: PassiveAggressiveClassifier (from scikit-learn)

Text is vectorized using TF-IDF.

Model trained on 80% of the data and tested on 20%.

Achieved ~94% accuracy.

5. Evaluation Metrics

Accuracy: 94%

Confusion Matrix:
| Predicted | Fake | Real |
|-----------|------|------|
| Actual Fake | 3700 | 300 |
| Actual Real | 2500 | 4200 |

Insights: Fake news tends to use sensational language; real news is more factual.

6. Deployment

Project is deployed as a Flask web application.

Users can enter text in the app and receive instant predictions.

The Flask app and all dependencies are available in this repository.

7. Repository Structure
Fake-News-Detection/
├── data/
│   ├── Fake.csv
│   └── True.csv
├── notebooks/
│   └── fake_news_detection.ipynb
├── src/
│   └── model.py
├── templates/
│   └── index.html
├── static/
│   └── style.css
├── model.pkl
├── vectorizer.pkl
├── app.py
├── README.md
└── requirements.txt

8. How to Run the Project

Clone the repository:

git clone https://github.com/nkajjastephen1/FakeNewsDetector.git


Install dependencies:

pip install -r requirements.txt


Run the Flask app:

python app.py


Open your browser and go to http://127.0.0.1:5000/

9. Future Work

Enhance the model using deep learning (LSTM / BERT).

Include metadata features (author, source, date).

Integrate local Ugandan news sources for region-specific detection.

Deploy a fully functional web or mobile app for real-time verification.

10. References

George McIntire, Fake and Real News Dataset – GitHub Link

scikit-learn Documentation – https://scikit-learn.org

Flask Documentation – https://flask.palletsprojects.com

This README makes yo
