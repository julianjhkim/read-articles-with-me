# Read Articles with Me

A Quarto book on reading, understanding, and simply replicating research papers.

📖 **Read the book:** https://julianjhkim.github.io/read-articles-with-me/

## Structure

```
.
├── _quarto.yml                  # book config & chapter list
├── index.qmd                    # preface
├── _templates/
│   └── paper-template.qmd       # copy this for each new paper
├── neuroai/                     # field
│   └── brain-encoding/          # subfield
│       └── YYYY-author-keyword.qmd
├── data/                        # small sample data only
├── _freeze/                     # cached code results (commit this!)
└── .github/workflows/publish.yml
```

## Adding a new paper

1. `cp _templates/paper-template.qmd <field>/<subfield>/2024-smith-keyword.qmd`
2. Add the file under its part in `chapters:` in `_quarto.yml`
   (one part per field/subfield, e.g. `"NeuroAI: Brain encoding"`)
3. `quarto preview` to write, then `quarto render` to update `_freeze/`
4. Commit (including `_freeze/`) and push → GitHub Actions publishes to `gh-pages`
