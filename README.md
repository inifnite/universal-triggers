# Universal Adversarial Triggers for Attacking and Analyzing NLP

Results mentioned in the Report can be found here:

```
https://colab.research.google.com/drive/1TwjDS5gIuwpHFN75Ti3HBWvB12G7LRUD?usp=sharing
https://colab.research.google.com/drive/1By5meXcFn0vLre5hMoKyanqQcqNwwKfK?usp=sharing
https://colab.research.google.com/drive/1V2GckVJpkD1gP2b7URaTn2Dc5-OJMXFj?usp=sharing
https://colab.research.google.com/drive/1LKQJRHkUV6YXAyBHt2FOJfeuPAXKi--U?usp=sharing
```

## Installation

An easy way to install the code is to create a fresh anaconda environment:

```
conda create -n triggers python=3.6
source activate triggers
pip install -r requirements.txt
```

## Getting Started

The repository is broken down by task: 
+ `sst` attacks sentiment analysis using the SST dataset (AllenNLP-based).
+ `snli` attacks natural language inference models on the SNLI dataset (AllenNLP-based).
+ `squad` attacks reading comprehension models using the SQuAD dataset (AllenNLP-based).
+ `gpt2` attacks the GPT-2 language model using HuggingFace's model.

To get started, we recommend you start with `snli` or `sst`. In `snli`, we download pre-trained models (no training required) and create the triggers for the hypothesis sentence. In `sst`, we walk through training a simple LSTM sentiment analysis model in AllenNLP. It then creates universal adversarial triggers for that model. The code is well documented and walks you through the attack methodology.

The gradient-based attacks are written in `attacks.py`. The file `utils.py` contains the code for evaluating models, computing gradients, and evaluating the top candidates for the attack. `utils.py` is only used by the AllenNLP models (i.e., not for GPT-2).


## References

```
@inproceedings{Wallace2019Triggers,
  Author = {Eric Wallace and Shi Feng and Nikhil Kandpal and Matt Gardner and Sameer Singh},
  Booktitle = {Empirical Methods in Natural Language Processing},                            
  Year = {2019},
  Title = {Universal Adversarial Triggers for Attacking and Analyzing {NLP}}
}    
```
