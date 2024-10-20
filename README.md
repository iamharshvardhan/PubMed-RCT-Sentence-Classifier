
# PubMed RCT Sentence Classifier

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRZ4K3IMdG9fQT-Fz-H1RypHhjDHVzLkC5_CA&s">

This project replicates research from two key papers focused on sequential sentence classification in medical abstracts, utilizing the **PubMed 200k RCT** dataset. The implementation focuses on sentence classification tasks using neural networks and aims to classify each sentence in medical research abstracts into categories like background, objective, methods, results, and conclusions.

The notebook replicates research on sequential sentence classification in medical abstracts, specifically focusing on two papers:

1. **Dataset Paper**: "PubMed 200k RCT: a Dataset for Sequential Sentence Classification in Medical Abstracts" [(arXiv Link)](https://arxiv.org/pdf/1710.06071)
2. **Model Paper**: "Neural Networks for Joint Sentence Classification in Medical Paper Abstracts" [(arXiv Link)](https://arxiv.org/pdf/1612.05251)

The content involves:

- Replication of the classification model using the provided dataset.
- Cloning of a GitHub repository (`pubmed-rct`), which contains datasets such as "PubMed_200k_RCT" and "PubMed_20k_RCT".

### Dataset
The notebook leverages the `PubMed_20k_RCT` and `PubMed_200k_RCT` datasets, which are downloaded and stored within the project. These datasets consist of files like `train.txt`, `dev.txt`, and `test.txt`, containing sentences annotated for classification tasks.

### Structure of the Notebook:
1. **Setup**: 
   - Cloning the necessary dataset repository and loading the files.
   - The datasets include both normal text and versions where numbers are replaced with an `@` symbol.
   
2. **Helper Functions**: 
   - Functions for loading data, such as `get_lines()` and `preprocess_text_with_line_numbers()`.
   - Utility functions to aid with TensorBoard, plotting loss curves, and comparing training histories.

3. **Data Preprocessing**:
   - The key function, `preprocess_text_with_line_numbers()`, extracts each abstract's sentences along with line number data and total line counts, creating a structured dataset for classification.

4. **Model Training**:
   - The notebook provides code for training neural networks using TensorFlow/Keras on the preprocessed data.
   - Callbacks for TensorBoard and model training tracking are provided through utility functions.

5. **Evaluation**:
   - After training, the model’s performance is evaluated on test data, comparing predicted labels to the true sentence labels.

### Requirements
- Python 3.x
- TensorFlow
- Keras

### How to Run
1. Clone the repository:
    ```bash
    git clone https://github.com/iamharshvardhan/PubMed-RCT-Sentence-Classifier.git
    ```
2. Download the necessary datasets.
    ```bash
    git clone https://github.com/Franck-Dernoncourt/pubmed-rct.git
    ```
3. Run the [notebook]("pubmed_rct_sentence_classifier.ipynb") in a Jupyter environment.

