# CITS4407 Assignment 2– Board Game Dataset Analysis

## 📄 Overview

Scripts completed for this project in accordance with the assignment-related requirements of CITS 4407.

The work is structured into three main scripts:

- `empty_cells`: identifies missing values in raw data.
- `preprocess`: cleans and transforms the dataset.
- `analysis`: performs statistical analysis on the cleaned data.

---

## 📄Scripts

### 1. `empty_cells`

Counts the number of empty fields in each column of the `bgg_dataset.txt`, which uses semicolon `;` as a delimiter.

#### ✅ Usage

```bash
./empty_cells bgg_dataset.txt
```

#### 🔧 Features

- Handles `;`-separated `.txt` input
- Strips Windows carriage returns (`\r`)
- Tolerates missing fields per row
- Outputs: `Column Name: Empty Count`

### 2. `preprocess`

Cleans the raw `.txt` dataset and outputs a standardized, tab-separated `.tsv` file for analysis.

#### ✅ Usage

```
./preprocess bgg_dataset.txt > bgg_clean.tsv
```

#### 🔧 Features

- Converts `;` to tab (`\t`)
- Removes Windows line endings (`\r`)
- Deletes non-ASCII characters
- Replaces commas with dots only in numeric columns (Rating Average & Complexity Average)
- Auto-generates unique IDs where missing

### 3. `analysis`

Analyzes the cleaned `.tsv` data and answers the four assignment research questions.

#### ✅ Usage

```
./analysis bgg_clean.tsv
```

#### 🔧 Outputs

1. Most popular game mechanic (by frequency)
2. Most popular game domain
3. Pearson correlation between:
   - Year Published and Rating Average
   - Complexity Average and Rating Average



## 📄Testing Datasets

Scripts have been tested using:

- `sample.txt`, `sample.tsv`
- `sample1.txt`, `sample1.tsv`
- `tiny_sample.txt`, `tiny_clean.tsv`

------



## 📄Git Usage

Version control was implemented using Git, with:

- Clear, staged commits for each phase of development
- Meaningful commit messages
- `.git` folder included in submission
