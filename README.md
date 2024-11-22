# **BERT Multilingual Word Masking**

**BERT Multilingual Word Masking** is a project implemented entirely in a python notebook. It demonstrates how to use the [BERT multilingual uncased model](https://huggingface.co/bert-base-multilingual-uncased) from Hugging Face Transformers for **masked word prediction**. The notebook allows users to input sentences, mask specific words, and get predictions for the masked positions.

---

## 🤔 **How Does It Work?**

This project leverages BERT's **masked language modeling (MLM)** capabilities to predict words based on their context in a sentence. The process incorporates special tokens required by the BERT model:

1. **Special Tokens**:
    
    - `[CLS]`: Added at the beginning of the input sentence. Represents a "classification token" used by BERT to understand the input context.
    - `[SEP]`: Added at the end of the input sentence to denote its end. This is essential when processing single or multiple sentences.
2. **Workflow**:
    
    - **Input Sentence**: The user provides a sentence where one or more words are replaced with `[MASK]` tokens.
    - **Tokenization**: The sentence is tokenized, including `[CLS]` at the start and `[SEP]` at the end.
    - **Model Input**: The processed tokens are fed into the BERT model.
    - **Predictions**: The model outputs probabilities for potential replacements of the `[MASK]` tokens.
    - **Output**: The notebook generates a detailed table with predictions and associated metadata.

---

## 🚀 **Key Features**

- **Interactive Notebook**: The entire workflow is contained within a single, user-friendly Jupyter Notebook.
- **Multilingual Support**: The model supports a wide variety of languages, including English, Spanish, French, and more.
- **Tokenization Strategy**: Incorporates `[CLS]` and `[SEP]` tokens to ensure compatibility with BERT.
- **Structured Output**: Results are presented in a table with detailed columns, including metadata.

---

## 📊 **Result Structure**

The output is a table with the following columns:

|**Column**|**Description**|
|---|---|
|`id`|Unique identifier for each prediction.|
|`owner`|Identifier for the origin or user of the data.|
|`model`|The BERT model used for the predictions.|
|`version`|Version of the model or system configuration.|
|`cod_audio`|(Optional) Code linked to audio data, if applicable.|
|`word`|The word in the original sentence that was masked.|
|`mask_qua`|Qualitative description of the mask or its context.|
|`mask_num`|Number of `[MASK]` tokens in the input.|
|`word_pos`|Position of the masked word within the input text.|
|`token`|Token ID predicted by BERT for the `[MASK]` token.|
|`token_str`|Decoded token string, representing the predicted word.|
|`token_score`|Probability score of the prediction for the masked position.|
|`word_match`|Boolean indicating if the predicted word matches an expected result (if defined).|


---

## 📋 **Technical Details**

|**Feature**|**Description**|
|---|---|
|**Model**|BERT multilingual uncased|
|**Framework**|Hugging Face Transformers|
|**Input Format**|Sentence(s) containing `[MASK]` tokens|
|**Output**|A detailed table with predictions and metadata|
|**Notebook Name**|`bert-base-multilingual-uncased.ipynb`|

---

## 💻 **How to Use**

1. **Install Dependencies**:  
    Install the required Python packages using:
    
    ```bash
    pip install transformers
    ```
    
2. **Run the Notebook**:  
    Open the notebook in Jupyter and follow the step-by-step cells to:
    
    - Input a sentence.
    - Mask one or more words using `[MASK]`.
    - View predictions displayed in a structured table.
3. **Example Input**:  
    _"Artificial intelligence is [MASK] for the future."_
4. **Example Output Table**:
    ![](https://i.imgur.com/Papmx4e.png)
---

## 📝 **Additional Notes**

- The `[MASK]` token identifies positions for prediction.
- `[CLS]` and `[SEP]` tokens ensure proper sentence processing and compatibility with BERT.
- Results include metadata for in-depth analysis, making it useful for research or development.

---

## 🎉 **That’s It!**
 
> This notebook provides an intuitive way to explore masked word prediction with BERT. Dive in and discover the possibilities!

---
