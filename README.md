# Fine-Grained Sentiment Detection in Code-Mixed Indian Languages

## Overview
This project focuses on **Fine-Grained Sentiment Detection** in code-mixed Indian languages (Hinglish, Tanglish, and Telglish) using state-of-the-art hierarchical multilingual contextual embeddings. The project compares the performance of **XLM-RoBERTa** and **MuRIL** (Multilingual Representations for Indian Languages) models to handle the linguistic complexities of code-switching between English and Indian languages.

## Project Structure
The project is organized into the following directories:

- **`CODE FILE/`**: Contains Jupyter Notebooks (`.ipynb`) for training and evaluating models.
  - `HINGLISH-XMLR&MURIL.ipynb`: Analysis and Model training for Hinglish data using both XLM-R and MuRIL.
  - `TANGLISH-XMLR.ipynb` / `TANGLISH-MURIL.ipynb`: Specialized notebooks for Tanglish (Tamil-English) data.
  - `TELGLISH-XMLR.ipynb` / `TELGLISH-MURIL.ipynb`: Specialized notebooks for Telglish (Telugu-English) data.

- **`DATASETS/`**: Contains the datasets used for training, validation, and testing.
  - `HINGLISHTRAIN.tsv`, `HINGLISHTEST.tsv`, `HINGLISHVALIDATE.tsv`: Data for Hindi-English code-mixed sentiment analysis.
  - `TANGLISH-DATASET.csv`: Data for Tamil-English code-mixed sentiment analysis.
  - `TELGLISH-DATASET.csv`: Data for Telugu-English code-mixed sentiment analysis.

## Datasets
The datasets are provided in TSV and CSV formats and typically include the following fields:
- `en_query`: The original query in English.
- `cs_query`: The code-switched query (e.g., Hinglish).
- `domain`: The domain of the query (e.g., alarm, weather, messaging).
- `Sentiment`: The sentiment label (e.g., `Positive`, `Negative`, `Neutral`).

Example entry:
| en_query | cs_query | Sentiment |
|----------|----------|-----------|
| set alarm for 2 hours | do ghante ke liye alarm set kardo | Negative |

## Models Used
1.  **XLM-RoBERTa (XLM-R)**: A transformer-based multilingual masked language model pre-trained on text in 100 languages.
2.  **MuRIL**: A BERT-based model pre-trained specifically on 17 Indian languages and their transliterated counterparts, making it highly effective for code-mixed Indian contexts.

## Usage
To run the experiments, open the respective `.ipynb` file in Jupyter Notebook or Google Colab.

### Prerequisites
Ensure you have the following libraries installed:
```bash
pip install transformers torch pandas scikit-learn numpy tqdm
```

### Running the Notebooks
1.  Navigate to the `CODE FILE` directory.
2.  Open the desired notebook (e.g., `HINGLISH-XMLR&MURIL.ipynb`).
3.  Update the file paths in the notebook to point to the correct location of the datasets in the `DATASETS` folder.
4.  Run all cells to train the models and view the evaluation results.

## Results
The notebooks compare the predictions of XLM-R and MuRIL against Ground Truth labels. Evaluation metrics such as Accuracy and F1-score are typically used to assess performance. Preliminary analysis suggests competitive performance between the two models, with MuRIL often showing superior understanding of cultural and linguistic nuances in code-mixed text.
