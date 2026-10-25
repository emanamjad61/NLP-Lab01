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

---

## Lab 02 — Data Acquisition

Notebook: [`NLP_Lab02.ipynb`](NLP_Lab02.ipynb)

All five in-lab activities and five home activities, run with outputs saved. The web
activities hit the live sites, so their numbers reflect the day the notebook was run.

**Activity 1 — Extracting Text from a PDF**
Opening a PDF in binary mode with PyPDF2 and joining every page's `extract_text()` into one raw string.

**Activity 2 — Headings vs Body in a Word Document**
Reading `.docx` paragraphs with python-docx and separating headings from body text by `style.name`.

**Activity 3 — Consuming a JSON API**
Calling a REST endpoint with `requests` and turning the response into Python lists and dictionaries.

**Activity 4 — Parsing an HTML Page**
Fetching raw HTML and using BeautifulSoup to pull out the page title and every hyperlink's text.

**Activity 5 — Scraping Repeated Records**
Collecting each book's title, link and price from the `product_pod` blocks on books.toscrape.com.

**Home Activities 1–5**
Top words from cleaned PDF text, paragraph length statistics from a `.docx`, average age per
department from the dummyjson users API, the Wikipedia population table cleaned into integers,
and multi-page quote scraping saved to JSON.

---

## Lab 03 — Regex, Tokenization & Sentence Segmentation

Notebook: [`NLP_Lab03.ipynb`](NLP_Lab03.ipynb)

**Activity 1 — Regex Fundamentals**
Groups, quantifiers and character classes to pull a username, domain and price out of text.

**Activity 2 — Extracting Contact Details**
`re.findall()` for order numbers, emails and phone numbers, with a stricter phone pattern.

**Activity 3 — Business Report Extraction**
Dates, percentages and revenue figures from a report, plus fixes for formats the first patterns miss.

**Activities 4 & 5 — Tokenizers and Pipelines**
NLTK vs spaCy word tokens, and why a blank spaCy pipeline tokenizes but assigns no tags or entities.

**Activity 6 — Token Attributes**
Filtering tokens with `is_alpha`, `like_num`, `like_email` and `is_currency` instead of regex.

**Activity 7 — Sentence Segmentation**
Splitting a paragraph into sentences with NLTK's Punkt and spaCy's parser.

**Home Activities 1–4**
Regex extraction from support tickets, token attributes vs regex for amounts, where NLTK and
spaCy tokenization differ, and flagging sentence-boundary disagreements.

<!-- LAB04-06 -->

---

## Lab 07 — POS Tagging & Named Entity Recognition

Notebook: [`NLP_Lab07.ipynb`](NLP_Lab07.ipynb)

**Activity 1 — Coarse vs Fine POS Tags**
spaCy's `.pos_` and `.tag_` for every token of a news paragraph, cross-checked against NLTK's tagger.

**Activity 2 — Context-Dependent Tagging**
"launch" tagged as a noun in "the launch event" and as a verb in "plans to launch the phone".

**Activity 3 — Filtering Noise Tokens**
A clean token/POS table without SPACE, PUNCT and X tokens, leaving the `Doc` itself unchanged.

**Activity 4 — Named Entities with displaCy**
Extracting `doc.ents`, highlighting them with displaCy, and counting entities per type.

**Activity 5 — Patching NER with EntityRuler**
Rules added before `ner` so "Pixel 10" and "iPhone" become PRODUCT, compared before and after.

**Home Activities 1–5 — Job Postings Pipeline**
POS statistics, entity counts by type, a custom SKILL rule, a word whose tag changes between
postings, and a structured company/location/skills extractor exported to CSV.

---

## Requirements

Lab 01 needs only the standard library. The later labs use:

```bash
pip install numpy pandas matplotlib scikit-learn nltk spacy requests beautifulsoup4 lxml PyPDF2 python-docx reportlab
python -m spacy download en_core_web_sm
```

Sample input files that the manual refers to but does not supply are created by the
notebooks themselves under `data/labNN/`.

```bash
git clone https://github.com/emanamjad61/NLP-Lab01.git
cd NLP-Lab01
jupyter notebook
```
