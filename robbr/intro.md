# RoBBR

[![RoBBR Paper](https://img.shields.io/badge/Paper-NeurIPS-blue.svg?logo=read-the-docs&logoColor=white)](https://link_to_your_paper) [![LEI Lab](https://img.shields.io/badge/Lab%20Group-LEI%20Lab-blue.svg?logo=teams&logoColor=white)](https://lei.ucsd.edu/) [![GitHub](https://img.shields.io/badge/GitHub-RoBBR-blue.svg?logo=github&logoColor=white)](https://github.com/RoBBR-Benchmark/RoBBR)

## Task Formulation

The RoBBR benchmark aims to provide an expert-validated tool for assessing whether models can accurately make risk of bias judgments for biomedical papers. This involves analyzing research study methodologies, evaluating the risk of bias, and providing expert-generated bias annotations. The benchmark follows the risk of bias framework developed by Cochrane and comprises four main tasks, derived from over 500 referenced papers. These tasks are designed to ensure a comprehensive evaluation of the models' capabilities in identifying and interpreting methodological strengths and weaknesses in biomedical studies.

### Benchmark Development

The benchmark is divided into **four main tasks**:

1. ``Study Inclusion/Exclusion`` Given the search protocol information and meta-analysis objective as input, determine whether a study should be included in the meta-analysis.

2. ``Bias Retrieval`` Retrieve sentences from the paper that support a judgment about the study's risk of bias.

3. ``Support Judgment Selection`` Reason with the retrieved information by choosing the judgment that best supports the determination of the study's risk of bias from a multiple-choice task.

4. ``Risk Level Determination`` Given the complete paper, the PICO of the study, the objective of the meta-analysis, and the definition of the bias, assess the study's overall risk of bias as high, low, or unclear.

### An Example

#### Search Protocol:

|                            |                                                                                                 |
| :------------------------- | :---------------------------------------------------------------------------------------------- |
| Types of Studies           | Randomized controlled trials (RCTs)                                                             |
| Types of Participants      | People living in leishmaniasis endemic regions.                                                 |
| Types of Interventions     | Any intervention that aims to reduce leishmaniasis incidence through vector or reservoir control. |
| Types of Outcome Measures  | - People developing CL or VL infections.<br> - Estimates of the vector density measured by an appropriate technique (adult sandfly density estimated by counts of vectors either landing on exposed body parts of humans acting as baits or collected resting inside buildings, for example, on walls).<br> - Number of participants with positive immunological or biochemical tests that detect contact with the parasite (for example, leishmanin skin test conversion rates or lymphocyte proliferation rates, or both).<br> - Adverse effects on people.<br> - Adherence to control measures; for example, the extent to which specified intervention components were delivered as prescribed.<br> - Measures of environmental impact (assessment of the possible impact - positive or negative - that the interventions may have on the natural environment) or sustainability (assessment of the ability to change biological and human processes, functions, biodiversity and productivity), or both. |



#### Objective of the Meta-Analysis:

To assess the effects of vector and reservoir control interventions for cutaneous and for visceral leishmaniasis.

#### Full Paper:

See [Werneck et al.](https://journals.plos.org/plosntds/article?id=10.1371/journal.pntd.0003172) for full paper content.

#### Bias Name and Definition:

**Bias name:** selective reporting (reporting bias) <br>

**Bias Definition:** reporting bias due to selective outcome reporting

#### PICO:

|         |                                                                                       |
| :-------------------- | :------------------------------------------------------------------------------------------------ |
| **Methods**           | **Trial design**: Cluster-RCT.<br> **Unit of randomization**: Geographic area.<br> **Number of clusters**: 40 geographic areas.<br> **Entomological data collection**: Not done.<br> **Clinical data collection**: Conversion of the Montenegro skin test (MST) at 18 months of follow-up.<br> **Length of follow-up**: 18 months.<br> **Analysis**: Analysed at cluster level. |
| **Participants**      | Ten localities in 7 neighbourhoods of the city of Teresina (Brazil) were divided into blocks, each containing an average of 60 residences. For each locality, 4 blocks were selected to minimize the risk of cross-contamination of interventions. Eligible participants were residents of selected blocks aged 1 year or above with no history of VL. The 40 geographic areas (blocks) randomly allocated to the 4 types of interventions (697 subjects MST-).<br> **Endemic disease**: VL caused by L. chagasi (L. infantum). |
| **Interventions**     | 1. Spraying households and residential annexes with insecticide.<br> 2. Elimination of infected dogs.<br> 3. Combination of spraying and eliminating infected dogs.<br> 4. No intervention.<br> **Description of spraying**: Performed according to the routine of the VL Control Program of the Zoonosis Control Center of the Teresina City Health Department. Interventions were delivered in the selected blocks every 6 months, for three times, beginning just after each household visit. The elimination of infected dogs was decided if indirect immunofluorescence test was more or equalled 1:40. |
| **Outcomes**          | Cases of infection by L. infantum at 18 months determined by conversion of the MST (MST- at the beginning) or diagnosis of active VL. |
| **Notes**             | **Country**: Brazil (Teresina, Itararé quarter).<br> **Trial dates**: January 2004 to December 2006.<br> **Trial sponsor**: Funded by Health Surveillance Unit from the Brazilian Ministry of Health. One author was partially funded by the Brazilian Research Council (CNPq 306267/2010-1 and 202088/2012-0). The founders had no role in trial design, data collection and analysis, decision to publish, or preparation of the manuscript. The authors have declared that no competing interests exist.<br> **Sample size**: Calculated.<br> **Compliance assessment**: Not reported. |
