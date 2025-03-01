# NER-Swahili

## Project Overview

NER-Swahili focuses on Named Entity Recognition (NER) for the Swahili language using the **AfriBERTa Large** model. The project utilizes the **MasakhaNER Dataset** to fine-tune and evaluate the model for Swahili entity recognition.

## About AfriBERTa

AfriBERTa is a transformer-based model trained on 11 African languages:

- Afaan Oromoo (Oromo)
- Amharic
- Gahuza (a mix of Kinyarwanda and Kirundi)
- Hausa
- Igbo
- Nigerian Pidgin
- Somali
- Swahili
- Tigrinya
- Yorùbá

AfriBERTa has been evaluated on NER and text classification tasks across multiple languages, including some it was not originally pretrained on.

## Dataset

We use the **MasakhaNER** dataset for training and evaluation.

- Dataset Link: [MasakhaNER on Hugging Face](https://huggingface.co/datasets/uestc-swahili/swahili)

## Implementation

The main implementation is in the `NLP_Project_Afriberta_Large.py` file.

### Dependencies

To run the project, install the required dependencies:

```bash
pip install transformers datasets seqeval evaluate
```

Additionally, import necessary libraries in your script:

```python
from transformers import Trainer, DataCollatorForTokenClassification
```

## How to Run the Code

### 1. Load the Dataset

While running the dataset loading code:

```python
from datasets import load_dataset
# Load the MasakhaNER dataset
dataset = load_dataset("masakhaner", "swa")
```

You will be prompted to type `Y` to proceed.

### 2. Train the Model

While running the fine-tuning cell:

```python
trainer.train()
```

You need to authorize access to Weights & Biases:

1. Click on **Get API Key** when prompted.
2. The link will redirect you to the Weights & Biases website.
3. Create an account using the **IIT Madras Zaniba Aluminization** group.
4. Copy and paste the provided API key in the required cell to continue.

Once authorized, the training will proceed smoothly.

## Output

After training and evaluation, the model extracts Named Entities and saves the results in an Excel file.

- **Output File:** `named_entities.xlsx`
- **File Structure:** The Excel file contains two columns:
  - **Entity**: The recognized named entity
  - **Type**: The corresponding NER category

## Usage

1. Install dependencies
2. Run the Python script: `python NLP_Project_Afriberta_Large.py`
3. Follow the instructions for dataset loading and API authorization.
4. Check `named_entities.xlsx` for extracted entities.

## Contact

For any inquiries, feel free to reach out!

