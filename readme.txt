# Intuitive Understanding


First, go through a text document(s) and count i words

Separate into sentences and append '[START]' and '[END]'

Create an empty matrix of i x i

Then, go through the text document(s) and count co occurences

This creates a sparse matrix with co-occurences including the start and end tokens


# To predict text:


Given a word, create a list of all words that have co-occured, inserted in the list the number of times they occurred. 

Choose from the list randomly, more frequent words will have a higher chance of being selected

To begin a sentence, prompt with the start token [START]


# Higher context windows:
TODO

Higher context windows will do the same as above, except for the matrix will include n previous words

So the matrix will have "it was __" on the co-occurence table, and counts the words occurring after "it was" (bi-gram)

This can work for higher n's, however larger contexts have a much higher chance of having sentences that have never occured. 

If some context has not been seen before, it will reduce the context window. 

