# CITS4407 Assignment 2: Board Games Analysis

## Scripts

- `empty_cells`: Count empty fields in a given column-separated file (default `;`).
- `preprocess`: Clean raw dataset (`.txt`) by converting to `.tsv` (tab-separated), removing non-ASCII characters, fixing decimal points, and assigning new IDs.
- `analysis`: Analyze cleaned dataset (`.tsv`) to determine:
  - Most popular mechanic and domain
  - Correlation between year and rating
  - Correlation between complexity and rating

## Usage

```bash
./empty_cells bgg_dataset.txt
./preprocess bgg_dataset.txt > bgg_clean.tsv
./analysis bgg_clean.tsv
