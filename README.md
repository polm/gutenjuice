# GutenJuice

This is a project to take popular books from Project Gutenberg and provide
their source text as well as extracted and classified keywords in a single
place. It may be useful for making silly twitter bots. 

The keyword extraction is performed using my
[chargen](http://github.com/polm/chargen) program, which relies on NLTK and
WordNet. 

The `src` directory contains the unmodified files from Project Gutenberg. 

The `extracted` directory contains JSON files that each contain a single object
with keys corresponding to the type of word. Unless otherwise noted, words
under a given word all have that word (in any sense) as a hypernym. 

- abstraction
- adjectives - Not hyponyms of adjective, just adjectives
- events
- food
- items - The hypernym here is "artifact" or "item"
- locations - The hypernym here is "location" or "structure", and words with the hypernym "body part" are excluded.
- people 
- trait

A note about the location keyword - if body parts are not excluded, words that
are normally only used as body parts but also sometimes used to describe
geographical features, particularly rivers, show up as locations. Examples are
"mouth", "butt", "neck". 

An effort has been made to remove bad results and to filter offensive terms,
but if you see anything left in please feel free to make a pull request or
notify me. In particular, pairs of words separated by unicode punctuation and
words consisting mostly of symbols may still be too numerous. 

-POLM 

WTFPL, do as you please. 
