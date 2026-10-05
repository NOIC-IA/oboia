# Impostor (OBOIA 2026, problem 3)

Problem by Ícaro Fróes. Find the 10 impostor pages hidden in SpongeBob's 3,000-page diary, with no labeled
training data.

| File | Português | English |
|---|---|---|
| Baseline (CLIP embeddings + t-SNE outliers) | [`baseline-ptbr.ipynb`](baseline-ptbr.ipynb) | [`baseline-en.ipynb`](baseline-en.ipynb) |
| Solution (CLIP zero-shot similarity per character) | [`solution-ptbr.ipynb`](solution-ptbr.ipynb) | [`solution-en.ipynb`](solution-en.ipynb) |

Each notebook starts with the full problem statement, scores itself on the public book, and ends with a bonus
section that runs the same method on the hidden book used for grading: its score, and a plot of the 10 pages
it picked, marking which ones are real impostors.

## Results

The notebooks are saved with their outputs. Scores from that run (Apple M5 Pro, CPU):

| | Public book | Hidden book |
|---|---|---|
| Baseline | 3/10 impostors, score 0.007 | 2/10 impostors, score 0.003 |
| Solution | 10/10 impostors, score 1.000 | 10/10 impostors, score 1.000 |

## Data

- `data/book_ans.csv`: the 10 impostor pages of the public book.
- `data/book_hidden_ans.csv`: the 10 impostor pages of the hidden book.
- `book.zip` and `book_hidden.zip` (about 1.1 GB each) are attached to the
  [`oboia-2026-impostor` release](https://github.com/NOIC-IA/oboia/releases/tag/oboia-2026-impostor).
  The notebooks download them into `data/` when they're missing.

Run the notebooks from this folder (they use `data/` as a relative path). A GPU helps; on Kaggle, turn on
**Internet** in the notebook settings.
