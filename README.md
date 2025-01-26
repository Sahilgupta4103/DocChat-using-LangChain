# DocChat-using-LangChain
Hugging face model used in this project 
Flan-T5


If you already know T5, FLAN-T5 is just better at everything. For the same number of parameters, these models have been fine-tuned on more than 1000 additional tasks covering also more languages. As mentioned in the first few lines of the abstract :

 Flan-PaLM 540B achieves state-of-the-art performance on several benchmarks, such as 75.2% on five-shot MMLU. We also publicly release Flan-T5 checkpoints,1 which achieve strong few-shot performance even compared to much larger models, such as PaLM 62B. Overall, instruction finetuning is a general method for improving the performance and usability of pretrained language models.

Disclaimer: Content from this model card has been written by the Hugging Face team, and parts of it were copy pasted from the T5 model card.

Model Details
Model Description
Model type: Language model
Language(s) (NLP): English, German, French
License: Apache 2.0
Related Models: All FLAN-T5 Checkpoints
Original Checkpoints: All Original FLAN-T5 Checkpoints
Resources for more information:
Research paper
GitHub Repo
Hugging Face FLAN-T5 Docs (Similar to T5)
Usage
Find below some example scripts on how to use the model in transformers:

Using the Pytorch model
Running the model on a CPU
Click to expand
Running the model on a GPU
Click to expand
Running the model on a GPU using different precisions
FP16
Click to expand
INT8
Click to expand
Uses
Direct Use and Downstream Use
The authors write in the original paper's model card that:

The primary use is research on language models, including: research on zero-shot NLP tasks and in-context few-shot learning NLP tasks, such as reasoning, and question answering; advancing fairness and safety research, and understanding limitations of current large language models

See the research paper for further details.

Out-of-Scope Use
More information needed.

Bias, Risks, and Limitations
The information below in this section are copied from the model's official model card:

Language models, including Flan-T5, can potentially be used for language generation in a harmful way, according to Rae et al. (2021). Flan-T5 should not be used directly in any application, without a prior assessment of safety and fairness concerns specific to the application.

Ethical considerations and risks
Flan-T5 is fine-tuned on a large corpus of text data that was not filtered for explicit content or assessed for existing biases. As a result the model itself is potentially vulnerable to generating equivalently inappropriate content or replicating inherent biases in the underlying data.

Known Limitations
Flan-T5 has not been tested in real world applications.

Sensitive Use:
Flan-T5 should not be applied for any unacceptable use cases, e.g., generation of abusive speech.

Training Details
Training Data
The model was trained on a mixture of tasks, that includes the tasks described in the table below (from the original paper, figure 2):

table.png

Training Procedure
According to the model card from the original paper:

These models are based on pretrained T5 (Raffel et al., 2020) and fine-tuned with instructions for better zero-shot and few-shot performance. There is one fine-tuned Flan model per T5 model size.

The model has been trained on TPU v3 or TPU v4 pods, using t5x codebase together with jax.

Evaluation
Testing Data, Factors & Metrics
The authors evaluated the model on various tasks covering several languages (1836 in total). See the table below for some quantitative evaluation:image.pngFor full details, please check the research paper.

Results
For full results for FLAN-T5-XXL, see the research paper, Table 3.

Environmental Impact
Carbon emissions can be estimated using the Machine Learning Impact calculator presented in Lacoste et al. (2019).

Hardware Type: Google Cloud TPU Pods - TPU v3 or TPU v4 | Number of chips ≥ 4.
Hours used: More information needed
Cloud Provider: GCP
Compute Region: More information needed
Carbon Emitted: More information needed
