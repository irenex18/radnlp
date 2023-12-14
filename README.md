The goal of this project is to create a text-to-text large language model that
is adept at several different classes of radiology tasks that may be relevant to
radiologists in their daily routines. Such a model could boost the productivity
of radiologists so that they could not only expedite results for a large patient
base, but so they can take more time to focus on patient care and satisfaction
as well. To create the main model of this project, we fine-tuned the Llama-2-
Chat 7 billion parameter model on impression generation and MRI/Pet/CT
classification tasks using Quantized Low Rank Adaptation (QLoRA) as a method
to improve memory efficiency when fine-tuning a large language model. For
impression generation, we found that the model fine-tuned on both anatomic
structures performed the best, with Rouge-L scores of 28.57 and 25.9 for chest
and pelvis impressions, respectively. Additionally, with the exception of MRI
classification, inference with models fine-tuned on several tasks resulted in
improved metrics compared to inference with the baseline model. This may
be because the MRI model over fit to the MRI training data, especially since
the average MRI classification reference sequences were much shorter than
those of the other datasets. Overall, the general model, which was fine-tuned
on all of the datasets mentioned above, performed best only for the Pet/CT
classification task, which makes sense since this was the last dataset that we
fine-tuned the model on. However, it seems like there’s promise in creating a
radiology foundation model, given a few changes in methodology.
