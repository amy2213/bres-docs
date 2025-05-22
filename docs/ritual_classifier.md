# Ritual Subtype Detection Classifier Module

This module enhances the Binary Ritual Encoding System (BRES) by introducing an integrated classifier capable of distinguishing between ritual subtypes across symbolic manuscripts. The classifier evaluates symbolic phase sequences and structural motifs to categorize artifacts into known ritual formats, including calendars, invocation sequences, astronomical registers, and others.

---

## Purpose

To move beyond phase decoding alone and offer automated classification of an artifact's function based on encoded symbolic structure. This enables:

- Faster identification of document type (e.g., calendar, ritual script, astronomical register)
- Subtype differentiation (e.g., solar vs. lunar calendars)
- Consistent labeling of new or uncertain manuscripts

---

## Classifier Structure

### Architecture
- **Input**: A tokenized phase stream (e.g., `['P', 'T', 'A', 'A', 'N', ...]`)
- **Features Extracted**:
  - Motif frequency distribution (e.g., PTAN, AATAA, etc.)
  - Closure pattern entropy
  - Invocation clustering density
  - Alternation signatures (e.g., A↔T transitions)
  - Total sequence length and boundary markers
- **Model**: Decision-tree backed symbolic classifier with Bayesian reinforcement
- **Output**: Predicted ritual subtype with confidence score (e.g., `"ritual calendar"`, 0.94)

---

## Subtypes Detected

| Subtype               | Key Indicators                                  |
|-----------------------|--------------------------------------------------|
| Ritual Calendar       | Regular closures, monthly cycles, PTAN motifs   |
| Invocation Script     | High invocation density, repeated A-pairings    |
| Astronomical Register | Phase drift, irregular closure, planetary sync  |
| Ceremonial Path Text  | Linear sequence with gateway motifs (P→T→A→N)   |
| Hybrid / Uncertain    | Mixed or ambiguous patterns                     |

---

## Training and Validation

- **Sample Data**: BRES-decoded sequences from:
  - Phaistos Disc
  - Coligny Calendar
  - Lead Plaque of Magliano
  - Dresden Venus Table
- **Synthetic Data**: 200+ modeled ritual sequences for robust training
- **Validation**:
  - Holdout cross-validation
  - Symbolic alignment scoring
  - Permutation tests (e.g., p < 0.01 for subtype clustering accuracy)

---

## Example Output

```json
{
  "artifact": "Phaistos Disc",
  "classification": "ritual calendar",
  "confidence": 0.91,
  "features": {
    "PTAN motifs": 5,
    "closures": 12,
    "invocation density": 0.32,
    "entropy": 0.72
  }
}
```

---

## Usage

1. Input a BRES-decoded phase sequence into the classifier.
2. The classifier analyzes structural and symbolic patterns.
3. It returns a ritual subtype and scores.

This enables researchers to treat undecoded artifacts more systematically and link them to known ceremonial archetypes.

---

## Next Steps
- Extend classifier with multilingual OCR phase mapping
- Integrate with GitHub-hosted BRES Toolkit CLI/Web version
- Add export tools (CSV/JSON) for batch artifact classification
