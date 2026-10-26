# Read Articles with Me

A Quarto book on reading, understanding, and simply replicating research papers.

📖 **Read the book:** https://julianjhkim.github.io/read-articles-with-me/

## Structure

```
.
├── _quarto.yml          # book config & chapter list
├── index.qmd            # preface
├── papers/
│   ├── 00-template.qmd  # copy this for each new paper
│   └── YYYY-author-keyword.qmd
├── data/                # small sample data only
├── _freeze/             # cached code results (commit this!)
└── .github/workflows/publish.yml
```

## Adding a new paper

1. `cp papers/00-template.qmd papers/2024-smith-keyword.qmd`
2. Add the file to `chapters:` in `_quarto.yml`
3. `quarto preview` to write, then `quarto render` to update `_freeze/`
4. Commit (including `_freeze/`) and push → GitHub Actions publishes to `gh-pages`
