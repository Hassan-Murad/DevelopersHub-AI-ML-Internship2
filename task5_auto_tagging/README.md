# Task 5: Auto-Tagging Support Tickets Using LLM

## Objective
The objective of this project is to automatically analyze free-text customer support tickets and assign the top-3 most probable category tags using a Large Language Model (LLM).

## Methodology / Approach
1. **Dataset Creation:** Formulated a realistic customer support ticket dataset spanning 10 predefined taxonomical categories (e.g., billing, technical issue, refund).
2. **Prompt Engineering:** Designed strict system prompts to enforce JSON-formatted outputs containing exactly three tags and their respective confidence scores.
3. **Zero-Shot vs. Few-Shot Testing:** Implemented and executed both zero-shot (instructions only) and few-shot (3-5 contextual examples) classification prompts.
4. **Evaluation:** Parsed the LLM's structured JSON responses and compared the accuracy metrics between the zero-shot and few-shot approaches.

## Key Results & Observations
* **Performance Comparison:** Few-shot prompting achieved a Top-1 Accuracy of ~90% and a Top-3 Accuracy of ~95%, noticeably outperforming the zero-shot approach (Top-1: ~80%, Top-3: ~90%).
* **Insights:** Providing the LLM with just a few formatting and reasoning examples (few-shot) significantly improved its ability to resolve ambiguous tickets (e.g., overlapping billing and refund requests).
* **Utility:** Forcing the LLM to output valid JSON with confidence scores makes this system highly viable for automated downstream triage and routing in a production support environment.