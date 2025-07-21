# Hindi Named Entity Recognition (NER) using BERT

This repository contains a Named Entity Recognition (NER) model implementation for the Hindi language using the WikiAnn dataset and the `bert-base-multilingual-cased` model from HuggingFace Transformers. The goal is to identify named entities like persons, organizations, and locations in Hindi text.

---

## Dataset

- **Source**: WikiAnn (Hindi)
- **Description**: WikiANN (sometimes called PAN-X) is a multilingual named entity recognition dataset consisting of Wikipedia articles annotated with LOC (location), PER (person), and ORG (organisation).
- **Format**: Each sample contains a list of `tokens` and their associated `ner_tags`, following the IOB2 labeling format.

---

## Model and Approach

- **Tokenizer**: `bert-base-multilingual-cased`
- **Model**: `AutoModelForTokenClassification` from HuggingFace Transformers

### Process Overview:

1. Load the dataset using the HuggingFace `datasets` library.
2. Tokenize input text while aligning entity labels to subword tokens.
3. Fine-tune the BERT model using the `Trainer` API.
4. Evaluate the model using standard classification metrics.

---

## Installation

Install the required libraries using pip:

```bash
pip install datasets
pip install tokenizers
pip install transformers
pip install seqeval
pip install --quiet "ipywidgets>=8,<9"
