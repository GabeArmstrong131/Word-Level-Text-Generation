# Word-level-Text-Generation

Word-level text generation in python using keras model and tensorflow.

Upload a text document that is then cleaned, prepared, and turned into sequences of 51 words (50 input and 1 output).

Words and sequences are tokenized using the keras tokenizer, mapping unique words to integers and encoding input sequences.

Sequences are then fit to a sequential language model. Accuracy is relative to the number of epochs, the size of the embedding vector space, and the number of neurons.

A randomized seed text is generated which is encoded using the same tokenizer that was used for input sequences. Each word is predicted as an integer using np.argmax(model.predict()) which is then mapped to the word from the tokenizer. The text is then fully generated.

With varying levels of accuracy in the model, some text generation is more realistic than others. Even with high accuracy there is a chance for the text to be nonsensical depending on the seed text and the model.
