## Feature Extraction

 (Structural Metrics)

Each artifact’s phase sequence is processed into a feature vector via `extract_bres_features_extended()`. Features include:
- Phase counts and proportions
- Shannon entropy
- Transition frequency matrix (e.g., A→T, T→P)
- Key motif counts (e.g., PTAN, ATAAN)
- Closure density
- Spatial glyph metadata (for spiral or radial artifacts)

---