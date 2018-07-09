### Introduction
We use the bidirectional recurrent neural networks (RNN) for the word-level representation,
and then apply the attention mechanism (Rocktäschel et al., 2015) to incorporate matching infor-
mation from question to passage at the word level. Next, we predict start and end positions of the
evidence snippet by pointer networks (Vinyals et al., 2015a). Moreover, we aggregate the word-level
matching information of each passage using the attention pooling, and use the passage-level representation to rank all candidate passages as an additional task. For the answer synthesis, we apply
the sequence-to-sequence model to synthesize the final answer based on the extracted evidence.
### Approach
evidence snippets extract + answer synthesis <br>
multi-task learning framework for evidence extraction <br>
sequence-to-sequence model with additional features of the start and end positions of the evidence snippet for the answer synthesis. <br>

##### Gated Recurrent Unit
Use GRU
##### Evidence Extraction
Use a multi-task learning framework.<br>
Improved text span prediction with passage ranking. <br>
In addition to predict text span,another task is to rank candidate passages with the passage-level representation.
###### Evidence Snippet Prediction