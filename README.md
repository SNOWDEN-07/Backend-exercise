It seems like I can’t do more advanced data analysis right now. Please try again later.

However, here's the updated **README.md** content with your GitHub username `SNOWDEN-07`:

---

```markdown
 📄 PubMed Paper Fetcher

A command-line tool to fetch research papers from PubMed based on a query, filter papers with at least one author affiliated with a pharmaceutical or biotech company, and export the results to a CSV file.

---

## 📁 Project Structure

```

pubmed\_fetcher/
├── pubmed\_fetcher/              # Core module
│   ├── **init**.py
│   ├── fetcher.py               # PubMed API interaction
│   ├── filters.py               # Heuristics for non-academic detection
│   └── utils.py                 # Helper utilities
├── cli.py                       # Command-line interface
├── pyproject.toml               # Poetry project config
├── README.md                    # Project documentation
└── tests/                       # Optional: unit tests

````

---

 🛠️ Installation & Setup

 Prerequisites:
- Python 3.8+
- [Poetry](https://python-poetry.org/) installed globally

 Install dependencies:
```bash
git clone https://github.com/SNOWDEN-07/pubmed-fetcher.git
cd pubmed-fetcher
poetry install
````

---

 🚀 Usage

Basic usage:

```bash
poetry run get-papers-list "cancer immunotherapy"
```

### Options:

| Option                               | Description                           |
| ------------------------------------ | ------------------------------------- |
| `-h`, `--help`                       | Show help message and exit            |
| `-f <filename>`, `--file <filename>` | Output CSV filename                   |
| `-d`, `--debug`                      | Enable debug logs for execution trace |

### Example:

```bash
poetry run get-papers-list "diabetes AND drug therapy" -f diabetes_papers.csv --debug
```

---

📦 CLI Entry Point

This project defines a CLI command using Poetry. You can run it using:

```bash
poetry run get-papers-list "<your query>"
```

Or if installed as a package:

```bash
get-papers-list "<your query>"
```

---

🔍 Output CSV Columns

| Column Name                | Description                                 |
| -------------------------- | ------------------------------------------- |
| PubmedID                   | Unique ID from PubMed                       |
| Title                      | Title of the research paper                 |
| Publication Date           | Date of publication                         |
| Non-academic Author(s)     | Authors with non-academic affiliations      |
| Company Affiliation(s)     | Name(s) of pharmaceutical/biotech companies |
| Corresponding Author Email | Email of the corresponding author           |

---

🧠 Tools and Technologies Used

| Tool/Library       | Purpose                                          |
| ------------------ | ------------------------------------------------ |
| `requests`         | Accessing PubMed E-utilities API                 |
| `lxml`             | XML parsing                                      |
| `argparse`         | Command-line interface                           |
| `csv`              | Output formatting                                |
| `Poetry`           | Dependency and packaging management              |
| `Git` + GitHub     | Version control                                  |
| `FPDF`             | PDF report generation                            |
| **OpenAI ChatGPT** | Assisted in code generation and heuristic design |

---

 📈 Heuristics for Non-Academic Filtering

Non-academic affiliations are detected using keyword heuristics such as:

* "Inc", "Ltd", "LLC", "Corporation", "Biotech", "Pharma", "Technologies"
* Email domains like `@pfizer.com`, `@novartis.com`

These are applied to author affiliations and email addresses to flag industry involvement.

---

 🧪 Testing

You can add unit tests under the `tests/` directory and run them using:

```bash
poetry run pytest
```

---

 ✍️ Author & License

Built by [SNOWDEN-07](https://github.com/SNOWDEN-07)
Licensed under the MIT License.

---

 📌 Notes

* Ensure a stable internet connection for PubMed API requests.
* API rate limits may apply. Please consult [NCBI E-utilities](https://www.ncbi.nlm.nih.gov/books/NBK25501/) documentation for more info.

---

```

Let me know if you'd like a downloadable version or want me to push this into a `.md` file again when the tools are available.
```
