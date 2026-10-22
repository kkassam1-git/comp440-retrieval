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

XXXX

## Part 3: Your own searches

### Your questions, as you typed them

XXXX

### Did the movies you meant come up? What did TF-IDF get right and wrong?

XXXX

## Part 4: The question bank

### Which kind of question did TF-IDF handle best, and which worst? By how much?

XXXX

### The misses you looked at: what do they have in common?

XXXX

## Part 5: Embeddings

### What is a sentence embedding, in your own words?

XXXX

### Where does each method do better, and why?

XXXX

### Your Part 0 predictions: which held, and which would you change?

XXXX

### How might you combine the two methods?

XXXX
