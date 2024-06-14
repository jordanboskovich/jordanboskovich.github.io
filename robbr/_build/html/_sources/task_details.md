# Task Details

The RoBBR Benchmark comprises several tasks, each designed to test a different aspect of a model’s capability to assess risk of bias accurately. Understanding these tasks can help in the development of more nuanced and effective AI tools.

## Task Overview

- **Study Inclusion/Exclusion**: Given the search protocol information and meta-analysis objective as input, determine whether a study should be included in the meta-analysis.
- **Bias Retrieval**: Retrieve sentences from the paper that support a judgment about the study’s risk of bias.
- **Support Judgment Selection**: Reason with the retrieved information by choosing the judgment that best supports the determination of the study’s risk of bias from a multiple-choice task.
- **Risk Level Determination**: Given the complete paper, the PICO of the study, the objective of the meta-analysis, and the definition of the bias, assess the study’s overall risk of bias as high, low, or unclear.

These tasks simulate real-world analytical processes that reviewers perform during systematic reviews, challenging models to interpret complex scientific texts and make judgements akin to those of human experts.
