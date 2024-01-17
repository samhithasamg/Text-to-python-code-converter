# CSCI-544-Project---Text-to-python-code-converter
Use of Transformers to convert Natural Language Text into Python code

Code generation transformers that are pretrained on large corpora of programs have shown great success in translating natural language to code. Although these models do not explicitly incorporate program semantics during training, they can create valid code snippets for many problems. In this project, we experiment on the translation potential of transformers and pre-trained transformers (CodeT5) in converting human languages to Python source code and gather results using BLEU evaluation. An analysis is presented to depict the outcomes of both methods. We observe a huge performance difference between the two models, with CodeT5 outperforming the base transformer and conventional recurrent-based architectures by a BLEU score of 49.06

## Dataset
We have trained the transformer models on the CoNaLa datase, which was created for the CMU CoNaLa (Code/Natural Language) challenge. CoNaLa is a manually curated dataset crawled from Stack Overflow. It consists of 2,739 training and 500 test examples. Each example consists of a question ID (ID of the Stack Overflow question), intent (the natural language intent), rewritten intent (incorporating function and variable names into the intent to better reflect the full meaning of the code), and a snippet (desired output)

## Evaluation
The results of the model are evaluated according to BLEU score after tokenization. BLEU has been frequently reported to correlate well with human judgement, and thus remains a benchmark for the assessment of any machine-translated text. Scores are calculated for individual translated code segments by comparing them with a set of executable code snippets. These scores are then averaged over the whole corpus to reach an estimate of the translation’s overall quality. Since BLEU assessment does not account for intelligibility or grammatical correctness, the metric is suitable for verifying code correctness. In addition, the CoNaLa challenge only accepts BLEU score results, hence the major focus was targeted towards one criterion.

## Implementation

Details and Flwowchart on Implementation can be found in Report
