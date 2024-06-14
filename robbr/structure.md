# RoBBR Structure

- ``task1_SIE_test.json`` and ``task1_SIE_dev.json``: Test and dev set of task 1 Study Inclusion/Exclusion
  - **paper_doi**: The DOI of the paper.
  - **objective**: The meta-analysis objective.
  - **search_protocol**: search protocol information of the meta-analysis.
  - **full_paper**: The full paper content.
  - **label**: One of [included, excluded], showing whether the paper is included or excluded in the meta-analysis.

- ``task2_ROBSR_test.json`` and ``task2_ROBSR_dev.json``: Test and dev set of task 2 Risk of Bias Sentence Retrieval
  - **paper_doi**: The DOI of the paper.
  - **bias**: The bias to be considered.
  - **PICO**: PICO of a study in the paper, including Methods, Participants, Intervention, Outcome, and Notes.
  - **objective**: The meta-analysis objective.
  - **paper_as_candidate_pool**: A tuple of text elements from the paper. Each text element is a sentence, a section title, a table, or a figure caption.
  - **aspects**: A dictionary that maps aspect id to bias aspect.
  - **aspect2sentence_indices**: A mapping (i.e., dictionary) between aspect id and all sentence indices that independently are source of information for that aspect, as annotated by our pipeline.
  - **sentence_index2aspects**: A mapping (i.e., dictionary) between sentence index and all aspect ids that this sentence is the source of information of.
  - **bias_retrieval_at_optimal_evaluation**: This is a dictionary that contains the necessary information for evaluating the model’s performance on the task Bias Retrieval @Optimal.
    - **optimal**: A positive integer, which is the smallest number of sentences needed to cover the largest number of aspects.
    - **one_selection_of_sentences**: A list of sentence indices. The list size is the optimal number. The list of sentences cover the largest number of aspects. Note, there are potentially other lists of sentences that have the same size and also cover the largest number of aspects.
    - **covered_aspects**: The list of aspects that are covered. In this case, the list of aspects covered is the list of all aspects.
  - **bias_retrieval_at_3_evaluation**: This is a dictionary that contains the necessary information for evaluating your model’s performance on the task Bias Retrieval @3.
    - **one_selection_of_sentences**: A list of 3 sentence indices. The list of sentences cover the largest number of aspects that can be covered under the restriction of 3 sentences. Note, there are potentially other lists of sentences that have size 3 and cover the same number of aspects.
    - **covered_aspects**: The list of aspects that are covered. In this case, this list of aspects may not be all the aspects. Since in the paper, we calculate aspect recall by dividing the number of aspects covered by model’s retrieved sentences against the total number of aspects, for Bias Retrieval @3, the maximum possible performance is not 100%.

- ``task3_SJS_test.json`` and ``task3_SJS_dev.json``: Test and dev set of task 3 Support Judgment Selection
  - **paper_doi**: The DOI of the paper.
  - **bias**: The bias to be considered.
  - **PICO**: PICO of a study in the paper, including Methods, Participants, Intervention, Outcome, and Notes.
  - **objective**: The meta-analysis objective.
  - **full_paper**: The full paper content.
  - **options**: The seven options for the multiple choice.
  - **label**: The index of the correct option.

- ``task4_RLD_test.json`` and ``task4_RLD_dev.json``: Test and dev set of task 4 Risk Level Determination
  - **paper_doi**: The DOI of the paper.
  - **bias**: The bias to be considered.
  - **PICO**: PICO of a study in the paper, including Methods, Participants, Intervention, Outcome, and Notes.
  - **objective**: The meta-analysis objective.
  - **full_paper**: The full paper content.
  - **label**: One of [low, high, unclear], representing the risk level of the bias.
