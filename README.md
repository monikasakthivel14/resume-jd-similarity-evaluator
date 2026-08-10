# resume-jd-similarity-evaluator
A zero-dependency, offline resume screening tool built using pure Python standard library to analyze and rank resumes against job descriptions.
# Offline Resume & Job Description Matcher

An efficient, lightweight, and fully offline resume screening tool designed to rank candidates against job descriptions without relying on external packages, libraries, or third-party APIs.

---

## Features
* **Zero External Dependencies:** Built using 100% Python Standard Library (`math`, `re`, `collections`, `csv`, `pathlib`, `argparse`).
* **Complete Data Privacy:** Fully offline execution ensuring candidate resume data remains secure and local.
* **Hybrid Matching Algorithm:** Combines **Cosine Similarity** (70% weight) and **Jaccard Index** (30% weight) with unigram and bigram extraction for accurate skill matching.
* **Keyword Gap Analysis:** Identifies matched skills alongside missing job description requirements.
* **Automated CSV Export:** Generates structured ranking reports for quick recruitment review.

---

## Project Structure

```text
offline-resume-matcher/
│
├── .gitignore
├── LICENSE
├── README.md
├── data/
│   ├── jd.txt
│   └── resumes/
│       ├── alex_developer.txt
│       └── sam_designer.txt
└── src/
    └── matcher.py
