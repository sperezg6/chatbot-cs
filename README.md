# Customer Service Chatbot

```markdown
# Customer Support Chatbot

This project demonstrates the process of building a customer support chatbot using Python and the Hugging Face Transformers library. The chatbot is trained on a dataset of conversation logs to understand and respond to customer inquiries.

## Installation

First, ensure that you have Python installed. Then, install the required libraries:

```bash
pip install transformers numpy pandas datasets sklearn torch logging accelerate
```

## Setting Up the Environment

The notebook automatically sets the computing device to GPU or CPU based on availability:

```python
device = 'cuda' if torch.cuda.is_available() else 'cpu'
print(device)
```

## Data Preparation

1. **Load your dataset**:
   Load conversation data from a CSV file.

2. **Data Preprocessing**:
   Perform text preprocessing such as lowercasing and NaN removal.

3. **Train-Test Split**:
   Split the conversation data into training and testing sets.

4. **Tokenization**:
   Tokenize the conversations for model training using `AutoTokenizer`.

## Parsing Conversations

Implement a function to separate customer inputs and agent responses from the conversation logs.

## Model Training

1. **Load Pre-Trained Model**:
   Use `AutoModelForSeq2SeqLM` from Hugging Face for the chatbot.

2. **Training Setup**:
   Configure training arguments and initialize a `Trainer` with the model and training dataset.

3. **Custom Metrics**:
   Include accuracy as a metric for model evaluation.

4. **Model Training**:
   Fine-tune the model on the conversation dataset.

## Model Saving and Uploading

Save the trained model and demonstrate how to upload it to a Hugging Face repository.

## Inference and Interaction

1. **Load the Model**:
   Instructions on how to load the model for inference.

2. **Generate Responses**:
   Implement a function to generate chatbot responses to user inputs.

3. **Interactive Testing**:
   Provide a script for interactive testing of the chatbot.

## Conclusion

This project illustrates the end-to-end process of building a conversational AI model using advanced NLP tools and techniques.
