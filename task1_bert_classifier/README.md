# Task 1: News Topic Classifier Using BERT

## Objective
The objective of this project is to fine-tune a pre-trained transformer model (`bert-base-uncased`) to classify news headlines into four distinct topic categories: World, Sports, Business, and Science/Technology. 

## Methodology / Approach
1. **Dataset:** Utilized the AG News dataset from Hugging Face for training and evaluation.
2. **Preprocessing:** Tokenized the text using the BERT tokenizer, applying truncation and padding for uniform input size.
3. **Model Fine-Tuning:** Fine-tuned the `bert-base-uncased` sequence classification model using the Hugging Face Trainer API.
4. **Evaluation:** Assessed the model's performance using Accuracy, F1-score, and a confusion matrix.
5. **Deployment:** Built and deployed an interactive, live-inference web interface using Gradio.

## Key Results & Observations
* **Performance:** The fine-tuned BERT model achieved approximately 94–96% test accuracy and a 94-96% weighted F1-score using an 8k training sample subset.
* **Insights:** The confusion matrix indicated that the model performs exceptionally well, with only minor expected misclassifications between closely related topics (e.g., World vs. Business).
* **Viability:** Transfer learning proved highly effective, demonstrating that a powerful pre-trained model can achieve production-level accuracy with relatively small domain-specific datasets.