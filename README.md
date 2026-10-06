# Fake News Detection Web App

A machine learning web application that classifies news articles as **real** or **fake**, built with **Python** and **Flask**.

> **Credit:** This project was built by following a tutorial, and the original code is by [Spidy20](https://github.com/Spidy20/Fake_News_Detection). I imported it into my own repo to study it, run it, and keep improving it.

---

## Screenshots

![Home page](s1.PNG)
![Prediction result](s2.PNG)

---

## Features

- Paste in a news headline or article text and get an instant prediction (real or fake)
- Trained text-classification model saved as `model.pkl`, so predictions load fast
- Simple Flask web interface (HTML templates and static CSS)
- Jupyter notebook showing the full training process step by step

---

## Tech Stack

| Area | Tools |
|------|-------|
| Language | Python 3 |
| Web framework | Flask |
| Machine learning | scikit-learn, pandas, NumPy |
| Frontend | HTML, CSS |
| Model storage | Pickle (`model.pkl`) |

---

## Project Structure

```
Fake_News_Detections/
├── static/                      # CSS and static assets
├── templates/                   # HTML pages for the web app
├── Fake_News_Det.py             # Flask app (run this file)
├── Fake_News_Detection.ipynb    # Notebook: data exploration and model training
├── model.pkl                    # Trained model
├── news.csv                     # Dataset of labeled news articles
├── requirements.txt             # Python dependencies
├── s1.PNG, s2.PNG, fn.jpg       # Screenshots and images
└── README.md
```

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/HasnainWorks/Fake_News_Detections.git
cd Fake_News_Detections
```

### 2. (Recommended) Create a virtual environment

```bash
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # macOS / Linux
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the app

```bash
python Fake_News_Det.py
```

Then open **http://127.0.0.1:5000** in your browser.

---

## How It Works

1. **Data:** `news.csv` contains news articles labeled as real or fake.
2. **Preprocessing:** the text is cleaned and converted into numerical features.
3. **Training:** a classifier is trained on those features and evaluated on a test set (see the notebook for the accuracy and confusion matrix).
4. **Deployment:** the trained model is saved to `model.pkl`. The Flask app loads it, takes the text a user submits, and returns the prediction.

---

## What I Learned

- How a text-classification pipeline works, from raw text to a prediction
- How to save and load a trained model with pickle
- How to connect a machine learning model to a Flask web app
- How to organize and publish a project on GitHub

---

## Future Improvements

- [ ] Retrain the model on a larger, more recent dataset
- [ ] Try other models and compare their accuracy
- [ ] Show a confidence score with each prediction
- [ ] Improve the UI design and make it mobile friendly
- [ ] Deploy the app online (Render, Railway, or similar)

---

## Acknowledgements

- Original project and tutorial by [Spidy20 (Kushal Bhavsar)](https://github.com/Spidy20)
- Contributions to the original repo by [root113](https://github.com/root113)

---

## Disclaimer

This model is for learning purposes. It predicts based on patterns in its training data and should not be used as a reliable fact-checking tool.

---

**Author:** [HasnainWorks](https://github.com/HasnainWorks)
