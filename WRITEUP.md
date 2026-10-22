# COMP 440: Representing and Retrieving Knowledge

Claude writes your answers here as you say them. A sentence or two is enough for each. Your
Part 0 predictions stay as you first wrote them; Part 5 asks what you would change.

**Name:** Kaif Kassam
**Date:** October 21, 2026

## Part 0: Predictions

### Questions that name a character, place or thing: which method will do better, and why?

im going to go with TF-IDF, specific names of movies or characters are more direct than embdedded meanings

### Vague descriptions: which method will do better, and why?

the embedding search works better for vague descriptions - since that's waht embdedding does, it compresses the question into general ideas

## Part 1: Build the TF-IDF model

### The settings you chose, and why

- `REMOVE_STOP_WORDS = False`: idf should shrink these commonly occuring "stop words" and their weights
- `MIN_MOVIES = 1`: anythign above this would make specific scenarios not workable, i.e. a movie name appears only in one summary and it is ignored because it is less than 2 appearances.
- `REPEATS_COUNT_LESS = True`: repeated count does not necessarily translate to higher relevance, especially given words that are not specific names.

## Part 2: Top terms

### Your movies: what do the top terms get right and wrong about what makes each one distinctive?

It gets specific names like vito and corleone right, but still weighs terms like launching, barely, and steps highly even if they contribute poorly to informing us about the movie.

## Part 3: Your own searches

### Your questions, as you typed them

1. A man travels on a mission to a nearby planet. A storm strikes and his team leaves him there thinking he is dead. He manages to survive and returns back eventually after setting communication with Earth.
2. A group of traders short the housing market after the financial crash of 2008.
3. A detective travels with a group of friends of someone really wealthy  who has anonymously invited him to an island. The friends play a game and people start dying. The detective has to solve this mystery.

### Did the movies you meant come up? What did TF-IDF get right and wrong?

The first one was spot on, the second one failed to have the movie in any of the top 10 listed, and the third one had the movie ranked number 4

It got right the matches where the meanings of words are not interchangeable - I would say the use of the word crash threw the algorithm off in the second search and the use of many common words like after, of, the, etc.

## Part 4: The question bank

### Which kind of question did TF-IDF handle best, and which worst? By how much?

TF-IDF did best on the questions that were detailed and had specific references like names of places, charactersm and things. It did the worst on reworded and close to that on vague questions. There is a 94% difference between the best and worst category.

### The misses you looked at: what do they have in common?

The misses I've looked at seem to include descriptions of similar ideas using different words - i.e. a difference between terms "rich" and "wealthy" or names like "cal" shared with other movies. This is inherently a failure of this algorithm that it depends on the frequency and matching of exact terms.

## Part 5: Embeddings

### What is a sentence embedding, in your own words?

XXXX

### Where does each method do better, and why?

XXXX

### Your Part 0 predictions: which held, and which would you change?

XXXX

### How might you combine the two methods?

XXXX
