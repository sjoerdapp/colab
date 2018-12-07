# Natural Language Sentiment Classification with Deep Learning
Assignment 2 (Sentiment Classification with Deep Learning) for the course "Natural Language Processing 1" at the University of Amsterdam

### Open ideas
- [x] Train standard LSTMs with attention modules 
  - _Result_: no (significant) improvement
  - _Problem_: too few data points to learn deep context / ignoring subtree annotation!
  - [ ] Train LSTM on short sequences/subtrees as well 
- [x] Training Tree LSTMs with subtrees
  - [x] Start with small trees/single words, and increase average tree height over time
  - [x] Record loss for subtrees, and take those with higher probability that have higher loss (over last _N_ iterations)
    - This list is shared across the same words and different trees
  - _Problem_: strongly imbalanced dataset, especially for small tree => MAF (see below)
  - [ ] Moving Average Filters for Loss Weighting
  - Which heuristic for determining the probabilities of tree heights at each iteration?
  - [x] Strong attention module/mechanism in Tree LSTMs
- [ ] Use context-free grammar rules to distinguish between different binary tree combinations (adjective and noun, verb and object, ...) and train different weights (might help) <= Need analysis of dataset first!
- [x] More detailed analysis during evaluation:
  - [x] How do we perform depending on the class?
  - [x] How do we perform depending on height fo the tree (and class)?
  - [x] Print out (small) examples during eval to understand prediction behaviour
  - [x] Print out the hardest/easiest training examples
- [ ] More detailed analysis of dataset
  - [x] Print example distribution over height
  - [x] Print class distribution depending on tree height
  - [ ] Consider frequency of examples when printing the class distributions
  - [ ] Print very common phrases/subtrees. Is there a pattern?
  - [ ] Try to annotate examples by POS tag, and find grammar rules for combining by binary tree. Is there something common/a pattern when a word (left or right) is more important?
  - [ ] Analyse the similarity of words (preinitialized values). Can we find synonyms between words? (High cosine-similarity and same humanly annotation?)
  - [ ] Check whether there are different annotations for same subtree in dataset (check for bugs in dataset).
# Reading and Writing Electronic Text

Notebooks and other materials for [Reading and Writing Electronic
Text](http://rwet.decontextualize.com/).

## Contents

### Session 01

* [Jupyter Notebook tutorial](jupyter-notebook-tutorial.ipynb)
* [Programming Exercise A](programming-exercise-a.ipynb)

### Session 02

* [Expressions and strings](expressions-and-strings.ipynb)
* [Some poetry generators](some-poetry-generators.ipynb)
* [Programming Exercise B](programming-exercise-b.ipynb)

### Session 03

* [Understanding lists, manipulating lines](understanding-lists-manipulating-lines.ipynb)

### Session 04

* [Poetics of grouping](poetics-of-grouping.ipynb)
* [Programming Exercise C](programming-exercise-c.ipynb)

### Session 05

* [Dealing with JSON](dealing-with-json.ipynb)

### Session 06

* [Tracery and Python](tracery-and-python.ipynb)

### Session 07

* [NLP Concepts with spaCy](nlp-concepts-with-spacy.ipynb)

### Session 08

* [N-grams and Markov chains](ngrams-and-markov-chains.ipynb) (Make sure to download the
  standalone version of the Markov chain code
  [here](https://gist.github.com/aparrish/14cb94ce539a868e6b8714dd84003f06))
* [Neural network text predition with textgenrnn](neural-network-text-prediction-with-textgenrnn.ipynb)

### Session 09

* [Understanding word vectors](understanding-word-vectors.ipynb)

### Supplementary material

* [Regular expressions in Python: a gentle introduction](regular-expressions-a-gentle-introduction.ipynb)
* [Quick and dirty keyword extraction](quick-and-dirty-keywords.ipynb)
* [Scraping HTML](scraping-html.ipynb)

### More TK

## License

Code and text examples in this repository are made available under the
following license:

    Copyright © 2018 Allison Parrish

    Permission is hereby granted, free of charge, to any person obtaining a copy of
    this software and associated documentation files (the “Software”), to deal in
    the Software without restriction, including without limitation the rights to
    use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
    of the Software, and to permit persons to whom the Software is furnished to do
    so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

