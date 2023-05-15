# NameError-name-tokenizer-is-not-defined
NameError: name 'tokenizer' is not defined: on jupyter notebook how to solve it.
!pip3 install transformers
from nltk.tokenize import word_tokenize
from transformers import AutoTokenizer

# encode X
word_tokenizer = Tokenizer()                         # instantiate tokenizer
word_tokenizer.fit_on_texts(X)                       # fit tokenizer on data
X_encoded = word_tokenizer.texts_to_sequences(X)     # use the tokenizer to encode input sequence

# Encode Y
tag_tokenizer = Tokenizer()
tag_tokenizer.fit_on_texts(Y)
Y_encoded = tag_tokenizer.texts_to_sequences(Y)

# look at first encoded data point

print("** Raw data point **", "\n", "-"*100, "\n")
print('X: ', X[0], '\n')
print('Y: ', Y[0], '\n')
print()
print("** Encoded data point **", "\n", "-"*100, "\n")
print('X: ', X_encoded[0], '\n')
print('Y: ', Y_encoded[0], '\n')
