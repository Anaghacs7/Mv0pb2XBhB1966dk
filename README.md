# Potential Talents — Candidate Ranking

An Apziva machine-learning project that ranks candidate job descriptions for a target human-resources role using text similarity and learning to rank.

## Objective

Build a candidate search and ranking workflow, reduce repeated job descriptions, and explore how starred candidates can influence subsequent rankings.

## Methods

- Inspect and clean the candidate dataset; validate IDs and handle repeated descriptions.
- Build a **TF–IDF** cosine-similarity baseline.
- Compare pretrained **Word2Vec** and **Sentence-BERT** semantic similarity.
- Review ranking agreement across the three representations.
- Mark starred candidates and train a **LightGBM ranker** on the selected similarity features.
- Display ranked candidates and feature importance.

## Repository layout

```text
Mv0pb2XBhB1966dk/
├── README.md
├── requirements.txt
├── .gitignore
├── GITHUB_UPLOAD.md
├── data/
│   └── README.md
└── notebooks/
    └── AP3_Potential_Talents_GBMRanker.ipynb
```

## How to run

1. Use Python 3.10+ and install packages: `pip install -r requirements.txt`.
2. Put the source CSV at `data/Potential_Talents_Aspiring_human_resources.csv`.
3. Start JupyterLab: `jupyter lab`.
4. Open `notebooks/AP3_Potential_Talents_GBMRanker.ipynb` and run the cells in order.

The Word2Vec and Sentence-BERT pretrained models may need an internet connection on first use and may require significant download time and disk space.

## Important limitations

The notebook can initialize starred labels from its own top-ranked descriptions. Those are **pseudo-labels**, not independent recruiter judgments. Any apparent improvement on those labels should not be presented as externally validated ranking quality. Evaluate with independent human relevance feedback and held-out queries before deployment.

Candidate screening can create fairness risks. Human review, role-relevant criteria, bias assessment, and privacy protections are necessary before operational use.

## Reproducibility

The notebook is included with its existing outputs, but the full pipeline has **not** been rerun in this package. Model downloads, source data, and environment setup are required.
