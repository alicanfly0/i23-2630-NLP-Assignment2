# i23-2630-NLP-Assignment2

**Author:** Ali Waseem (23i-2630)


This repository contains the complete PyTorch implementation of a Neural NLP Pipeline for a BBC Urdu corpus, built entirely from scratch without the use of pre-trained models or high-level transformer libraries.

## Repository Structure
This repository mirrors the required submission structure:
* `i23-2630_Assignment2_DS-6A.ipynb`: The main execution notebook.
* `embeddings/`: Contains saved numpy matrices and vocabulary mappings.
* `models/`: Contains the PyTorch `.pt` state dictionaries for the trained models.
* `data/`: Contains the generated CoNLL format train/test splits.

## Environment Setup
To run this project, ensure you have Python 3.8+ installed along with the following primary dependencies:

`pip install torch numpy matplotlib scikit-learn`

## How to Reproduce

**Part 1: Word Embeddings**
1. Place `cleaned.txt` and `raw.txt` in the root directory.
2. Run the Part 1 execution block in the Jupyter Notebook.
3. The script will automatically generate and save `tfidf_matrix.npy`, `ppmi_matrix.npy`, and `embeddings_w2v.npy` to the `embeddings/` folder.

**Part 2: Sequence Labeling (BiLSTM-CRF)**
1. Ensure the outputs from Part 1 are available.
2. Run the Part 2 execution block.
3. The script will parse the corpus into sentences, annotate them, and train the POS and NER BiLSTM models. 
4. Model weights will be saved to the `models/` folder.

**Part 3: Transformer Encoder**
1. Ensure `Metadata.json` and `cleaned.txt` are in the root directory.
2. Run the Part 3 execution block.
3. The script will train the custom Transformer model for 5-class topic classification and output the final test metrics and confusion matrix.
