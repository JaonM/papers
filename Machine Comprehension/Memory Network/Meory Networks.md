# Meory Networks
https://arxiv.org/pdf/1410.3916.pdf
### Introduction
* Memory in traditional RNN is too small.
* The central idea is to combine the successful learning strategies developed in the machine learning literature for inference with a memory component that can be read and written to

### MEMORY NETWORKS
 A memory network consists of a memory $\boldsymbol{m}$ (a list of vectors or strings) and four components *I*,*G*,*O* and *R*. <br>
 I: (input feature map) – converts the incoming input to the internal feature representation. <br>
 G: (generalization) – updates old memories given the new input. We call this generalization as there is an opportunity for the network to compress and generalize its memories at this stage for some intended future use.
 <br><br>
 Model Flows:<br>
 (1) Convert $x$ to an internal feature representation $I(x)$.<br>
 (2) Update memories $\boldsymbol{m}_i$ given the new input: $\boldsymbol{m}_i=G(\boldsymbol{m}_i,*I(x)*,\boldsymbol{m}),\forall{i}$ <br>
 (3) Compute the output features $o$ given the new input and the memory: $o:=O(I(x),m)$ <br>
(4) Finally, decode output features $o$ to give the final response: $r=R(o)$

### A MEMNN Implentation For Text
##### Basic Model

