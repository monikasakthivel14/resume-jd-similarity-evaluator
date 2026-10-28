# Resume-JD Similarity Evaluator

A Python-based tool that compares resumes against a job description, calculates similarity scores, identifies missing keywords, ranks candidates, and exports the results to CSV.

## Features

- **Resume ranking:** Ranks resumes according to their similarity to a job description.
- **Weighted similarity scoring:** Combines cosine similarity (70%) and Jaccard similarity (30%).
- **Keyword gap analysis:** Identifies relevant keywords from the job description that are missing from each resume.
- **CSV export:** Saves comparison results for further analysis.
- **Offline processing:** Processes local text files without external APIs.
- **No third-party dependencies:** Uses Python's standard library.

## Technologies Used

- Python
- Text processing
- Cosine similarity
- Jaccard similarity
- CSV file handling

## Project Structure

```text
resume-jd-similarity-evaluator/
├── data/
│   ├── jd.txt
│   └── resumes/
│       ├── resume1.txt
│       └── resume2.txt
├── src/
│   └── main_python_file.py
├── README.md
└── .gitignore
```

*The resume filenames above are examples. Keep the actual filenames already present in your repository.*

## Getting Started

### 1. Prerequisites

Install Python 3. No additional Python packages are required.

### 2. Prepare the input files

- Add the target job description to `data/jd.txt`.
- Place the resume text files (`.txt`) inside `data/resumes/`.

### 3. Run the evaluator

From the repository's root directory, run:

```bash
python src/main_python_file.py --jd data/jd.txt --resumes data/resumes --out results.csv
```

### 4. Review the results

The program exports the comparison results to `results.csv`. Review the similarity scores, rankings, and keyword gaps to understand how closely each resume matches the job description.

## How Scoring Works

The evaluator combines two text similarity measures:

**Final Score = (0.70 × Cosine Similarity) + (0.30 × Jaccard Similarity)**

- **Cosine similarity:** Measures similarity between text representations based on their word features.
- **Jaccard similarity:** Measures overlap between sets of extracted text features.

The weighted score helps compare resumes consistently against the same job description.

## Limitations

- Results depend on the text available in the input files.
- Similarity scores are not a measure of a candidate's complete ability or suitability.
- The tool does not replace human review or make hiring decisions.
- The scoring method is a project-defined heuristic, not a validated recruitment assessment.

## Future Improvements

- Add automated unit tests.
- Support PDF and DOCX resume extraction.
- Add configurable scoring weights.
- Create a simple web interface for comparing resumes.

## Author

**Monika S**

[GitHub](https://github.com/monikasakthivel14) · 
[LinkedIn](https://www.linkedin.com/in/monika-s-877767389/)
