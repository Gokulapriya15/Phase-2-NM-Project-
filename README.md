EXPOSING THE TRUTH WITH ADVANCED FAKE NEWS DETECTION POWERED BY NATURAL LANGUAGE 

1. OVERVIEW 

This project implements a fake news detection system using deep learning and natural language processing (NLP). It classifies news articles as "Real" or "Fake" based on their content using an LSTM-based neural network. The system supports multiple input methods and includes tools for model evaluation and retraining.

---

2. FEATURES 

Cleans and preprocesses news text using NLP techniques

Uses an LSTM model for accurate classification

Accepts input via:

1.Raw text

2.File path

3.Web URL

Automatically loads a saved model or trains a new one

Fetches and processes text from a URL

Generates a confusion matrix to visualize performance

---

3. REQUIREMENTS 

Install the following dependencies using pip:

pip install pandas numpy tensorflow matplotlib seaborn scikit-learn nltk beautifulsoup4 requests

---

4. DATASET FILES
   
Fake.csv and True.csv inside the data/ or root project folder

---

5. How It Works

Data Preprocessing:

1.Converts text to lowercase

2.Removes special characters and numbers

3.Applies lemmatization and stopword removal

4.Tokenizes and pads sequences for model input

Model Architecture:

1.Embedding Layer

2.LSTM Layer

3.Dropout Layer

4.Dense Output Layer (Sigmoid Activation)

5.Trained for 5 epochs with batch size of 32

Model Handling:

If fake_news_model.h5 exists, it loads directly

If not, the model trains from scratch and saves the trained version

---

6. USAGE

Running the Program

Run the script in terminal:

python main.py

Input Methods

Raw text input via terminal

File path to a .txt file with news content

URL of a news article (fetches and processes HTML content)

---

7. EXAMPLE OUTPUT 

Enter a news article (text, file path, or URL) or type 'exit' to stop:
https://example.com/fake-news-article

Checking the URL...
Prediction probability: 0.12
This news is FAKE


---

8. MODEL EVALUATION 

After training, the script generates a confusion matrix:

sns.heatmap(cm, annot=True, fmt='d', cmap='Blues')
plt.xlabel('Predicted')
plt.ylabel('Actual')
plt.title('Confusion Matrix')
plt.show()




---



