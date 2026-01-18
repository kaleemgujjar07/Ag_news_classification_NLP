# AG News Classification — TF-IDF + Classical NLP

**Goal:** Classify news headlines/articles into 4 categories (World, Sports, Business, Sci/Tech) using classical NLP techniques (no deep learning).

**Objectives:**
- Explore the dataset and class distribution.
- Build a robust text-cleaning pipeline.
- Extract TF-IDF features with n-grams (uni/bi/tri).
- Train and compare Logistic Regression, MultinomialNB, and LinearSVC.
- Evaluate on validation and test sets; save best model + vectorizer.

## Dataset
Place `train.csv` and `test.csv` in the same folder as the notebook before running. The notebook will attempt to detect title/description/label columns automatically.

## Requirements
Install Python packages from `requirements.txt`.

Quick install (recommended in a virtualenv or Colab cell):

```bash
pip install -r requirements.txt
```

> Note: The notebook includes a `files.upload()` step intended for Google Colab. Running locally you can skip the upload prompts if `train.csv`/`test.csv` are already present.

## Usage
1. Open `Ag_news_classification_NLP.ipynb` in Colab or Jupyter.
2. Install dependencies (run the pip cell or use `pip install -r requirements.txt`).
3. Upload or place `train.csv` and `test.csv` in the notebook directory.
4. Run cells top-to-bottom. The notebook will:
   - Load and inspect the dataset
   - Clean and combine text fields into a `text` column
   - Build TF-IDF features (n-grams)
   - Train and evaluate classical classifiers (Logistic Regression, MultinomialNB, LinearSVC)
   - Save the best model and vectorizer using `joblib`

## Output
- Trained model and TF-IDF vectorizer files (saved via `joblib`) — check the notebook for exact filenames.

## Notes
- This notebook uses NLTK resources (stopwords, wordnet, punkt); the notebook downloads them at runtime.
- If running outside Colab, remove or adapt the `google.colab` upload cell.

---

Generated from `Ag_news_classification_NLP.ipynb`.