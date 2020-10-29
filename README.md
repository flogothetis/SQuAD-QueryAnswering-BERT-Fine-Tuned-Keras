# SQuAD-QueryAnswering-BERT-Keras (TPU)
A context-based query answering model trained by leveraging Hugging-Face pretrained model.


## What is SQuAD?

Stanford Question Answering Dataset (SQuAD) is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text, or span, from the corresponding reading passage, or the question might be unanswerable.

SQuAD2.0 combines the 100,000 questions in SQuAD1.1 with over 50,000 unanswerable questions written adversarially by crowdworkers to look similar to answerable ones. To do well on SQuAD2.0, systems must not only answer questions when possible, but also determine when no answer is supported by the paragraph and abstain from answering.
(https://rajpurkar.github.io/SQuAD-explorer/)

## Implementation details:

Hugging Face's Bert pretrained model was used. Creating a Bert capable of SQuAD problem demands a classification layer at the top. The model output is consisted of two probabilities for each token. The former is the probability of starting the answer from token_i, and the last is the probability that token_i is the final token of the answer. For illustation purposes the folling image is given:

<img src="https://miro.medium.com/max/1840/1*QhIXsDBEnANLXMA0yONxxA.png" />

## Run on Google colab
1. Open Google Colab
2. Load .ipnb file 
3. Set hardware to TPU
4. Run all cells

