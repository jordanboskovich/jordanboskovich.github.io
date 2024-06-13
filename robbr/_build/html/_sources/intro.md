# RoBBR

[![EvidenceBench Paper](https://img.shields.io/badge/Paper-NeurIPS-blue.svg?logo=read-the-docs&logoColor=white)](https://link_to_your_paper) [![LEI Lab](https://img.shields.io/badge/Lab%20Group-LEI%20Lab-blue.svg?logo=teams&logoColor=white)](https://lei.ucsd.edu/) [![GitHub](https://img.shields.io/badge/GitHub-EvidenceBench-blue.svg?logo=github&logoColor=white)](https://github.com/RoBBR-Benchmark/RoBBR)

## Task Formulation

The RoBBR benchmark aims to provide an expert-validated tool for assessing whether models can accurately make risk of bias judgments for biomedical papers. This involves analyzing research study methodologies, evaluating the risk of bias, and providing expert-generated bias annotations. The benchmark follows the risk of bias framework developed by Cochrane and comprises four main tasks, derived from over 500 referenced papers. These tasks are designed to ensure a comprehensive evaluation of the models' capabilities in identifying and interpreting methodological strengths and weaknesses in biomedical studies.

### Benchmark Development

RoBBR is derived from 63 Cochrane meta-analyses and 532 papers referenced in those meta-analyses. The benchmark is divided into four main tasks:

1. ``Study Inclusion/Exclusion`` Given the search protocol information and meta-analysis objective as input, determine whether a study should be included in the meta-analysis.

2. ``Bias Retrieval`` Retrieve sentences from the paper that support a judgment about the study's risk of bias.

3. ``Support Judgment Selection`` Reason with the retrieved information by choosing the judgment that best supports the determination of the study's risk of bias from a multiple-choice task.

4. ``Risk Level Determination`` Given the complete paper, the PICO of the study, the objective of the meta-analysis, and the definition of the bias, assess the study's overall risk of bias as high, low, or unclear.
