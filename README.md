# GenerativeAI_NB

Notebooks on generative AI and modern NLP models.

## Notebooks

| Notebook | What it covers |
|---|---|
| [bert_sentiment_analysis](notebooks/bert_sentiment_analysis.ipynb) | Fine-tunes `bert-base-uncased` with Hugging Face Transformers and PyTorch to classify the emotion of tweets (SMILE Twitter Emotion dataset): data cleaning, stratified split, tokenization, training loop, weighted F1 and per-class accuracy. |

## Setup

```bash
git clone https://github.com/navendu10/GenerativeAI_NB.git
cd GenerativeAI_NB
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

1. Download the dataset and put `smile-annotations-final.csv` in `data/`. See [`data/README.md`](data/README.md).
2. Open `notebooks/bert_sentiment_analysis.ipynb` and run the cells in order.
3. Training uses a GPU if one is available (`cuda`) and falls back to CPU, which is very slow for 10 epochs.
   Checkpoints are saved to `models/` after every epoch.

## Repository layout

```
.
├── notebooks/
│   └── bert_sentiment_analysis.ipynb
├── data/                  # dataset goes here (git-ignored) + README
├── models/                # created when training runs (git-ignored)
├── requirements.txt
├── LICENSE
└── README.md
```

## License

[MIT](LICENSE). The SMILE dataset has its own terms; see its figshare page.
