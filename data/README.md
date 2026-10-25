# Data

The dataset is not tracked in git. Download it and place the file here:

| File | Used by | Source |
|---|---|---|
| `smile-annotations-final.csv` | `notebooks/bert_sentiment_analysis.ipynb` | SMILE Twitter Emotion dataset, Wang, Tsakalidis, Liakata, Zubiaga, Procter and Jensen (2016), figshare: <https://doi.org/10.6084/m9.figshare.3187909.v2> |

The file has no header row; the notebook reads it with the columns `id`, `text` and `category`.

Expected layout:

```
data/
├── README.md
└── smile-annotations-final.csv
```

Trained checkpoints are written to `models/` (git-ignored, created automatically by the notebook).
