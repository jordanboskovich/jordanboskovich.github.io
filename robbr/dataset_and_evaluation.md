# Dataset and Evaluation Metrics

## Dataset Overview

The RoBBR dataset includes data from 63 Cochrane meta-analyses and 532 biomedical papers. It has been meticulously annotated for various biases, providing a diverse and comprehensive resource for training and testing AI models.

### Details

- **Train/Test Split:** 23 randomly selected meta-analyses and their 228 corresponding papers were put in the dev set. The other 40 meta-analyses and their corresponding 304 papers are in the test set.
- **Annotation Process:** Support judgments containing specific claims about the study are mapped to specific sentences within the paper using GPT-4. Then, all 2221 support judgment aspects are manually inspected to ensure they relate to specific information from the paper. 
- **Evaluation Strategy:** Chain-of-thought prompting is used to stabilize the model performance. Prompts are optimized on a separate development set.

## Evaluation Metrics

To ensure a comprehensive assessment, several metrics are used to quantify the performance of AI models against expert human judgments:

- **Bias Recall @ 3 (BR@3)**: Measures the proportion aspects covered when three sentences are retrieved.
- **Bias Recall @ Optimal (BR@Optimal)**: Measures recall when the “optimal" number of sentences are retrieved. The optimal number of sentences is defined as the fewest which are sufficient to cover all bias aspects.
- **Accuracy**: Measures the precision of inclusion/exclusion decisions, correct bias retrieval, and risk determination.
- **Weighted Accuracy**: Adjusts the accuracy metric to account for the varying significance of different types of errors in the evaluation process.
- **Macro-F1**: Averages the F1-scores of various categories, providing a balanced measure across tasks where categories may be unevenly represented.

These metrics help ensure that the tools developed using the RoBBR benchmark are both effective and reliable.

```{note}
Each task within the RoBBR benchmark utilizes these metrics differently to best reflect the specific challenges they present:
- **Task 1** (Study Inclusion/Exclusion): Accuracy, Weighted Accuracy, and Macro-F1
- **Task 2** (Bias Retrieval): Bias Recall @ 3 and Bias Recall @ Optimal
- **Task 3** (Support Judgment Selection): Accuracy 
- **Task 4** (Risk Level Determination): Accuracy and Weighted Accuracy
