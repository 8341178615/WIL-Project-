# COSC2669 WIL Project – Employee HR Policy RAG Assistant

A test-driven Retrieval-Augmented Generation (RAG) prototype for employee HR policy support. The system retrieves relevant policy information, generates source-backed answers, handles unsupported questions through refusal/escalation, and records evaluation results.

## Project Overview

The prototype uses a small fictional HR policy knowledge base to test whether employees can receive fast and relevant answers to common workplace questions.

The project includes:
- HR policy data preparation and text chunking
- Semantic retrieval using sentence embeddings
- Answer generation using a local language model
- Source tracking and refusal handling
- Test questions for both answerable and out-of-scope cases
- Retrieval, latency and response-outcome evaluation

## Repository Structure

```text
COSC2669-WIL-HR-Policy-RAG/
├── Employee_HR_Policy_RAG_Full_Colab_Reference.ipynb
├── Employee_HR_Policy_Dataset_SAMPLE.csv
├── HR_RAG_Outputs/
│   ├── metrics_summary.json
│   ├── rag_test_results.csv
│   ├── rag_source_chunks.csv
│   ├── test_questions_and_expected_answers.csv
│   ├── human_review_TO_COMPLETE.csv
│   ├── retrieval_quality.png
│   ├── response_outcomes.png
│   └── latency_by_question.png
└── README.md
```

## Main Test Results

- Knowledge base: 8 fictional HR policy documents
- Prepared text chunks: 28
- Test questions: 25
  - 20 answerable questions
  - 5 out-of-scope questions
- Retrieval Hit@1: 75%
- Retrieval Hit@3: 95%
- Relevant-source fraction@3: 73.33%
- Average response time: approximately 1.33 seconds
- Correct refusal rate for out-of-scope questions: 80%

These results demonstrate retrieval performance only. Human verification of answer correctness and faithfulness should be completed before making reliability claims.

## How to Run

1. Open `Employee_HR_Policy_RAG_Full_Colab_Reference.ipynb` in Google Colab.
2. Upload or connect the HR policy dataset when prompted.
3. Run the notebook cells in order, or use **Runtime → Run all**.
4. The notebook processes the policies, creates embeddings, retrieves relevant passages, generates answers, evaluates the system and saves result files.
5. Review the generated files in the `HR_RAG_Outputs` folder.

## Human Review

The file `human_review_TO_COMPLETE.csv` is provided for manual evaluation of:
- factual correctness
- faithfulness to retrieved sources
- source relevance
- safety appropriateness
- reviewer notes

## Important Note

The HR policy dataset used in this project is fictional and is intended only for academic demonstration. The prototype must not be used as real HR, legal, employment or contractual advice.

## Course

**COSC2669 – Case Studies in Data Science**  
**WIL Project – Group 11**
