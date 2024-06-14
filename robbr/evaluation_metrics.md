# Evaluation Metrics

Aspect-level recall metrics measure the proportion of the bias aspects that are covered by the retrieved sentences. They are used to evaluate the performance of a model in retrieving sentences from a paper that support bias judgments.

## Bias Recall @ 3 (BR@3)

BR @ 3 measures the proportion aspects covered when three sentences are retrieved.

## Bias Recall @ Optimal (BR@Optimal)

BR @ Optimal measures recall when the “optimal" number of sentences are retrieved. The optimal number of sentences is defined as the fewest which are sufficient to cover all bias aspects.

### Evaluation Metric Breakdown by Task

**Task 1:** ``macro-F1``, ``accuracy``, and ``weighted accuracy``

**Task 2:** ``BR @ 3`` and ``BR @ Optimal``

**Task 3:** ``accuracy``

**Task 4:** ``accuracy`` and ``weighted accuracy``

---

```{note}
**Chain-of-thought** prompting is used to stabilize the model performance. Prompts are optimized on a separate development set.
```

---

## Notes

- **Dataset Sources:** RoBBR is derived from 63 Cochrane meta-analyses and 532 papers referenced in those meta-analyses.
- **Train/Test Split:** 23 randomly selected meta-analyses and their 228 corresponding papers were put in the dev set. The other 40 meta-analyses and their corresponding 304 papers are in the test set.
- **Annotation Process:** Support judgments containing specific claims about the study are mapped to specific sentences within the paper using GPT-4. Then, all 2221 support judgment aspects are manually inspected to ensure they relate to specific information from the paper. 