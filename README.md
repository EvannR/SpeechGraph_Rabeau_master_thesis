# SpeechGraph — Master's Thesis

Analysis of speech graph metrics in individuals with **Schizophrenia Spectrum Disorder (SSD)** compared to healthy controls.

Each participant verbally described 9 picture sequences across 3 difficulty levels. Their transcripts were converted into directed speech graphs, and structural metrics were extracted to characterize narrative cohesion, lexical connectivity, and speech complexity.

## Notebooks

| Notebook | Description |
|---|---|
| `visualization.ipynb` | Build speech graphs from raw transcripts and compute metrics → outputs `data_SpeechGraph2.csv` |
| `0_groupes.ipynb` | Descriptive analysis of verbal production length (SSD vs. controls) |
| `0_metrics.ipynb` | Correlation analysis between speech graph metrics and production variables |
| `1_interactions.ipynb` | Linear mixed models: Group × Difficulty Level effects on LSCC, AD, ASPL |
| `2_facility.ipynb` | Correlations between graph metrics and perceived ease (Cayouette scores) |
| `3_commonality_analysis.ipynb` | Commonality analysis: speech graph vs. symptoms predicting perceived ease (SSD only) |

## Metrics

| Metric | Definition |
|---|---|
| `n_tokens` | Total tokens (gross speech length) |
| `n_nodes` | Unique words (lexical diversity) |
| `n_edges` | Unique word transitions |
| `LSCC` | Largest Strongly Connected Component size |
| `AD` | Average Degree (edges / nodes) |
| `ASPL` | Average Shortest Path Length within the LSCC |

## How to run

```bash
python -m venv .venv
.venv\Scripts\activate      # Windows
pip install -r requirements.txt
jupyter notebook
```

Run `visualization.ipynb` first to generate `data_SpeechGraph2.csv`, then the other notebooks in any order.

## Data

Raw transcripts and clinical data are not included in this repository (participant privacy). The precomputed file `data_SpeechGraph2.csv` must be generated locally from the source data.

## Author

Evann Rabeau — Master's thesis, VITAM research group
