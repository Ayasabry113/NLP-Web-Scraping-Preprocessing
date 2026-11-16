# Web Scraping and Text Preprocessing

A Natural Language Processing fundamentals project that scrapes paragraph text from two web pages and applies a standard preprocessing pipeline.

## Source pages
- [New Cairo — Wikipedia](https://en.wikipedia.org/wiki/New_Cairo)
- [RMS Titanic Inc. — Research and Conservation](https://rmstitanicinc.com/research-and-conservation/)

## Pipeline
1. Fetch page HTML using `requests`.
2. Parse HTML and extract non-empty paragraph elements using BeautifulSoup.
3. Convert text to lowercase.
4. Remove numbers, punctuation, and special characters.
5. Tokenize text with NLTK.
6. Remove English stopwords.
7. Calculate token statistics and unique words.
8. Export processed paragraphs and statistics to CSV.


## Run locally
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook
```
Open the notebook and run all cells from top to bottom. An internet connection is required to retrieve the web pages and download NLTK resources on first run.

## Generated outputs
The notebook creates an `outputs/` directory containing:
- `preprocessed_paragraphs.csv`
- `unique_words.csv`
- `preprocessing_statistics.csv`

These files are generated during execution and are not required in the GitHub repository.

## Notes
- The notebook extracts paragraph (`<p>`) elements only.
- Website content and HTML structure can change; scraping results may vary over time.
- The cleaning pipeline keeps English letters and whitespace, removes numbers and punctuation, and uses NLTK's English stopword list.
- This project demonstrates web scraping and preprocessing; it does not train an NLP model.
- Follow each website's terms, robots.txt guidance, and reasonable request limits.

## Technologies
Python, Requests, BeautifulSoup, NLTK, Pandas, Jupyter.
