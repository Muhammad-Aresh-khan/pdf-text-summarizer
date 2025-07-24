# PDF Summarizer

A simple Python script to extract and summarize text from PDF files using `PyPDF2` and `nltk`. This tool reads a PDF, extracts its text, and produces a concise summary by ranking sentences according to word frequency.

---

## Features

- **PDF Text Extraction**: Reads and extracts text from PDF files.
- **Automatic Summarization**: Generates a summary by selecting the most relevant sentences.
- **Dependency Auto-Installer**: Installs required packages (`PyPDF2` and `nltk`) if missing.
- **Stopwords and Tokenization**: Utilizes NLTK for sentence and word tokenization, as well as stopword filtering.

---

## Requirements

- Python 3.x

The script will install the required dependencies automatically if they are not present:
- [PyPDF2](https://pypi.org/project/PyPDF2/)
- [nltk](https://pypi.org/project/nltk/)

---

## Installation

1. **Clone the repository or download the script:**
   ```bash
   git clone <your-repo-url>
   # or just download pdf summarizer.py
   ```

2. **Place your PDF file**  
   Put the PDF you want to summarize in the same directory as the script and name it `sample.pdf`, or adjust the filename in the script.

---

## Usage

Run the script from the command line:

```bash
python "pdf summarizer.py"
```

By default, the script will:
- Summarize the content of `sample.pdf` in the same folder.
- Print a summary of the 5 most relevant sentences.

**If you want to summarize a different file:**  
Edit the line in the script:
```python
pdf_path = r"sample.pdf"
```
and set it to your PDF filename.

---

## How It Works

1. **Dependency Check**:  
   The script checks for and installs `PyPDF2` and `nltk` if not already installed.

2. **Text Extraction**:  
   Reads all pages from the PDF and extracts text.

3. **Summarization**:  
   - Tokenizes the text into words and sentences.
   - Removes common stopwords.
   - Scores sentences based on the frequency of significant words.
   - Selects the top `max_sentences` (default 5) as the summary.

---

## Customization

- **Number of Sentences**:  
  To change the number of sentences in the summary, modify the `max_sentences` parameter in the function call:
  ```python
  summary = summarize_text(text, max_sentences=3)
  ```

- **PDF File Path**:  
  Change the `pdf_path` variable to the desired PDF file.

---

## Example Output

```
--- Summary ---

[Summary text will appear here]
```

---

## Notes

- The quality of the summary depends on the structure and clarity of the PDF's text.
- Some PDFs with scanned images or unusual formatting may not be summarized accurately.
- For best results, use PDFs with selectable, machine-readable text.

---

## License

This project is open-source and free to use under the MIT License.

---

## Troubleshooting

- **No text extracted**: The PDF might be image-based (scanned). Try using OCR tools first.
- **NLTK errors**: If you encounter issues with downloading NLTK data, ensure you have internet access on first run.

---

## Contributions

Pull requests and suggestions are welcome!
