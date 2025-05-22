# Binary Ritual Encoding System (BRES)

This repository contains all documentation and source material for the BRES system, including:

- Ritual classification and symbolic phase mapping (P, T, A, N)
- Artifact analysis (Phaistos Disc, Venus Table, etc.)
- Interpretation pipeline and developer implementation guide

---

## Structure

```
/docs               # MkDocs content
mkdocs.yml          # Site configuration
README.md           # This file
```

---

## Local Deployment (MkDocs)

1. Install MkDocs and the Material theme:
   ```bash
   pip install mkdocs mkdocs-material
   ```

2. Preview the site locally:
   ```bash
   mkdocs serve
   ```

3. Open [http://localhost:8000](http://localhost:8000) in your browser.

---

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository.
2. Run:
   ```bash
   mkdocs gh-deploy
   ```

Your documentation will be published at:
```
https://<your-username>.github.io/<your-repo-name>/
```

---

## License & Credits

All code and content is © 2025 Amy Laird (DataWeaver). Licensed for academic and research use only. Synthetic datasets are labeled and annotated within the `docs/` sections.

Developed with assistance from OpenAI's GPT-4 architecture.