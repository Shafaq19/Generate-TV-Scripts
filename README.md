# Generate-TV-Scripts
In this project, I'll generate Seinfeld TV scripts using RNNs and part of the Seinfeld dataset of scripts from 9 seasons.
## Installation 
If you are using pip then you can install the required libraries by:

 `pip install -r requirements.txt`

Conda users can make use of the env.yml file to activate

  `conda env create -f env.yml`

   `conda activate env.yml`

## Usage
- [x] Load the model

  `trained_rnn = helper.load_model('./save/trained_rnn')`

- [ ] To generate the text, the network needs to start with a single word and repeat its predictions until it reaches a set length. You'll be using the generate function to do this. It takes a word id to start with, prime_id, and generates a set length of text, predict_len. Also note that it uses topk sampling to introduce some randomness in choosing the most likely next word, given an output set of word scores!

    `import numpy as np`

    `gen_length = 400 # modify the length to your preference`

    `prime_word = 'elaine' # name for starting the script`

    `pad_word = helper.SPECIAL_WORDS['PADDING']`

    `generated_script = generate(trained_rnn, vocab_to_int[prime_word + ':'], int_to_vocab, token_dict, vocab_to_int[pad_word], gen_length)`

    `print(generated_script)`

## Credits
Shafaq Arshad @udacity NanoDegree
