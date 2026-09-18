# Natural Language Processing — Lab Work

Coursework repository for the **Natural Language Processing** lab.

**Eman Amjad** · FA23-BAI-013

---

## Lab 01 — Python Essentials for NLP

Notebook: [`NLP_Lab01.ipynb`](NLP_Lab01.ipynb)

All nine lab tasks (36 parts in total) are solved in one Jupyter notebook. Each part
has its own code cell with the output already saved, so the notebook can be read
directly on GitHub without running it first.

### What each task covers

**Task 01 — Strings as Text Storage**
Holding a sentence in a `str`, slicing out words, negative indexing, substring
searches with `in` and `index()`, and splitting a multi-line paragraph into sentences.

**Task 02 — Lists for Token Management**
Storing tokens in order, growing and shrinking the list with `append()`, `insert()`
and `remove()`, joining two token lists, and sorting alphabetically versus by length.

**Task 03 — Dictionaries for Word Mapping**
Word-frequency tables, adding and deleting entries, and building a reverse
`id -> word` lookup from a `word -> id` vocabulary.

**Task 04 — Sets for Unique Vocabulary**
Deduplicating a token list, set union / intersection / difference, and using set
difference to strip stopwords out of a sentence.

**Task 05 — Tuples for Fixed Linguistic Data**
Word/POS-tag pairs, tuple unpacking, the `TypeError` that immutability produces,
and a function that filters tagged pairs down to nouns.

**Task 06 — String Cleaning Methods**
`strip()`, `lower()`, `replace()`, `split()` and `join()` chained into a text
normalisation function.

**Task 07 — String Validation Methods**
`startswith()`, `endswith()`, `find()`, and classifying tokens as words, numbers
or mixed with `isalpha()` and `isdigit()`.

**Task 08 — Functions and Lambda for NLP Pipelines**
Regular functions next to their lambda equivalents, then composing them into a
single reusable preprocessing pipeline.

**Task 09 — map(), filter(), sorted() and Counter**
Transforming and filtering token lists functionally, sorting by different keys, and
counting word frequencies with `collections.Counter`.

### Requirements

Only the Python standard library is used — nothing needs to be installed.

```bash
git clone https://github.com/emanamjad61/NLP-Lab01.git
cd NLP-Lab01
jupyter notebook NLP_Lab01.ipynb
```
