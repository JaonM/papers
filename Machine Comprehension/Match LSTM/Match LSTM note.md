### Introduction
Predicted answer is a span in paragraph.<br>
Match-LSTM + Pointer Net(Ptr-Net) <br>
* We propose two new end-to-end neural network
models for machine comprehension, which combine match-LSTM and Ptr-Net to handle the special
properties of the SQuAD dataset.
* We have achieved the performance of an exact match score of 67.9% and an F1 score of 77.0% on the unseen test dataset, which is much better than the feature-
engineered solution (Rajpurkar et al., 2016)

### Method
#### MATCH-LSTM
Obtain a weighted vector representation of the premise.the weighted premise is then to  be combined with a vector representation of the current token of the hypothesis and fed to an LSTM.
#### POINTER NET
Ptr-Net uses attention mechanism as a pointer to select a position from input sequence as an output symbol.
#### Paper Method
Passage is represented by matrix $\boldsymbol{P}\in R^{d\times P}$ P is the length of passage and d is the dimentionality of word embeddings. <br>
The paper represent the answer as a sequence of integers $\boldsymbol{a}=(a_1,a_2,...)$ where $a_i\in(1,P)$ indicates a certain position in the passage. <br>

**Three layers**<br>
1. An LSTM preprocessing layer that preprocesses the passage and the question using LSTMs.
2. A match-LSTM layer that tries to match the passage against the question.
3. An Answer Pointer (Ans-Ptr) layer that uses Ptr-Net to select a set of tokens from the passage as the
answer.


