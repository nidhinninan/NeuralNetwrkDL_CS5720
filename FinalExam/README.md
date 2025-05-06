# Final Exam: Neural Network & Deep Learning

**Github Repo Link:** https://github.com/nidhinninan/NeuralNetwrkDL_CS5720.git 

**Name:** Nidhin Ninan

**ID:** 700772413

## **File:** `FinalExam_NNDL_NidhinNinan.py`  
**Video Link**: [https://drive.google.com/file/d/1-PJnPSKpMet6rLEpqPgZcZ6vEQEcLVKL/view?usp=sharing](https://drive.google.com/file/d/1yQ9eMqIJEPZsuWjEQvwh-EK_MG3Il37d/view?usp=drive_link)

## Overview

This Jupyter Notebook walks you through training, saving and loading an LSTM-based sentiment analysis model. You will:

* Load and preprocess text data (`Data.csv`).
* Build, compile and train an LSTM model in Keras/TensorFlow.
* Save the trained model and preprocessing artifacts (tokenizer, label encoder).
* Load those artifacts and run predictions on new raw text.

## Prerequisites

* **Python** ≥ 3.7
* **Jupyter Notebook** or JupyterLab

### Python Packages

Install the required packages via pip:

```bash
pip install pandas numpy scikit-learn scikeras tensorflow matplotlib
```

> *Note: The notebook also uses `keras` imports. The `tensorflow` package provides Keras by default.*

## Files

* `FinalExam_NNDL_NidhinNinan.ipynb` — the main notebook
* `Data.csv` — raw dataset with two columns:

  * `text` (string)
  * `sentiment` (label)

After you run the notebook, it will generate:

* `sentiment_model.h5` — saved Keras model
* `tokenizer.pickle` — fitted `Tokenizer`
* `label_encoder_classes.npy` — NumPy array of label classes

## Setup

1. Clone or download this repository.
2. Place `Data.csv` in the same folder as the notebook.
3. Create and activate a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate      # macOS/Linux
   venv\Scripts\activate.bat     # Windows
   ```
4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   *(Or use the pip command above if you don’t have a `requirements.txt`.)*

## Usage

1. Launch Jupyter:

   ```bash
   jupyter notebook FinalExam_NNDL_NidhinNinan.ipynb
   ```
2. Run all cells in order.
3. When prompted, inspect training output and ensure the model trains without errors.
4. After training, the notebook saves:

   * The LSTM model (`.h5`)
   * The tokenizer (`.pickle`)
   * The label encoder classes (`.npy`)
5. In the “Model Loading & Prediction” section, call `predict_sentiment(raw_text)` on any string to get:

   * **Predicted label** (e.g. “Positive”, “Negative”, “Neutral”)
   * **Probability scores** for each class

### Example

```python
from tensorflow.keras.models import load_model
import pickle, numpy as np

# Load artifacts
model      = load_model('sentiment_model.h5')
tokenizer  = pickle.load(open('tokenizer.pickle','rb'))
classes    = np.load('label_encoder_classes.npy')

# Preprocess & predict
def predict_sentiment(text):
    seq = tokenizer.texts_to_sequences([text])
    padded = pad_sequences(seq, maxlen=MAX_LEN)
    probs = model.predict(padded)[0]
    label = classes[np.argmax(probs)]
    return label, dict(zip(classes, probs))

sentiment, probabilities = predict_sentiment("I love learning with ChatGPT!")
print(sentiment)          # e.g. Positive
print(probabilities)      # {'Negative': 0.02, 'Neutral': 0.10, 'Positive': 0.88}
```

## Notebook Structure

1. **Imports & Data Loading**
   Load `Data.csv`, explore the text and label distributions.
2. **Preprocessing**

   * Clean text (regex, lowercasing)
   * Tokenize and pad sequences
   * Encode labels
3. **Model Building & Training**

   * Define `Sequential` LSTM architecture
   * Compile with `Adam` optimizer and categorical cross-entropy
   * Train with a validation split
4. **Saving Artifacts**

   * Save model (`.h5`)
   * Serialize tokenizer (`.pickle`)
   * Export label classes (`.npy`)
5. **Loading & Prediction**

   * Load saved model and artifacts
   * Define and test `predict_sentiment` on sample strings

## Contributing

* Feel free to submit improvements via pull requests.
* For major changes, please open an issue first to discuss your ideas.

## License

This work is released under the MIT License.

---

*Author: Nidhin Ninan*
*Date: May 2025*

