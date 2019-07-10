
Conceptually they differ from a standard neural network as the standard input in a RNN is a word instead of the entire sample as in the case of a standard neural network. This gives the flexibility for the network to work with varying lengths of sentences, something which cannot be achieved in a standard neural network due to it’s fixed structure. It also provides an additional advantage of sharing features learned across different positions of text which can not be obtained in a standard neural network.

there are three other types of architectures of RNN which are commonly used.

1. **Many to One RNN** : Many to one architecture refers to an RNN architecture where many inputs (Tx) are used to give one output (Ty). 
ex : classification task

2. **One to Many RNN**: One to Many architecture refers to a situation where a RNN generates a series of output values based on a single input value. 
ex : music generation

3. **Many to Many Architecture ** (Tx not equals Ty): This architecture refers to where many inputs are read to produce many outputs, where the length of inputs is not equal to the length of outputs. 
ex : machine translation

Limitations :
- Examples of RNN architecture stated above are capable of capturing the dependencies in only one direction of language. Basically in case of Natural Language Processing it assumes that the word coming after has no effect on the meaning of the word coming before. With our experience of languages we know that it is certainly not true.
- RNN are also not very good in capturing long term dependencies and the problem of vanishing gradients resurface in RNN.

Both these limitations give rise to new types of RNN architectures 
* Gated Recurrent Unit
* LSTM
* Bidirectional RNN
