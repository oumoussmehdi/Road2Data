## BERT : Bidirectional Encoder Representations from Transformers

language model developed and released by Google in late 2018. 
Pre-trained language models like BERT play an important role in many natural language processing tasks, such as : 
- Question Answering
- Named Entity Recognition 
- Natural Language Inference 
- Text Classification

BERT is a multi-layer bidirectional Transformer encoder based on fine-tuning. 

* Seq2Seq model : The model is divided into the encoder layer and the decoder layer, and is composed of RNN or RNN variants (LSTM, GRU, etc.). 
The main bottleneck of the Seq2Seq model is the need to compress the entire contents of the source sequence into a fixed-size vector. 
If the text is slightly longer, it is easy to lose some information of the text. 
In order to solve this problem, Attention came into being. 


he attention mechanism alleviates this problem by allowing the decoder to look back at the source sequence hidden state, 
and then provide its weighted average as an additional input to the decoder. 

Using Attention, as its name suggests, the model selects the context that best fits the current node as input during the decode phase. 

There are two main differences between Attention and the traditional Seq2Seq model: 
1. First, the encoder provides more data to the decoder, and the encoder will provide the hidden state of all nodes to the decoder, not just the hidden state of the last node of the encoder.
2. Second, the decoder does not directly use the hidden state provided by all encoders as input, but adopts a selection mechanism to select the hidden state that best matches the current position.

Transformer model uses the encoder-decoder architecture.

* Self-Attention
* Multi-Headed Attention 

- Positional Encoding
- Residual Connection and Layer Normalization
- Decoder
- Output layer
- BERT

# ref 
https://towardsdatascience.com/breaking-bert-down-430461f60efb
