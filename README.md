### Dataset
This project uses the [Motley Fool Earnings Call Transcripts](https://www.kaggle.com/datasets/tpotterer/motley-fool-scraped-earnings-call-transcripts) dataset.  
Place the downloaded `motley-fool-data.pkl` in the `data/` folder before running the notebooks.


# Earnings Call NLP: Analyst-Focused Summarization and Sentiment Analysis

## Overview
Earnings call transcripts are a rich source of information for investors, but they are lengthy, repetitive, and time-consuming to review. This project applies Natural Language Processing (NLP) techniques to **automatically summarize earnings calls**, providing analysts with a concise, structured synopsis of management commentary.

As the project evolves, additional NLP layers are introduced to analyze **sentiment, tone, and risk-related language**, enabling deeper insight into how information is communicated—not just what is said.

---

## Business Motivation
Equity and credit analysts routinely review dozens of earnings calls each quarter. Manual review is:
- Time intensive
- Inconsistent across analysts
- Difficult to scale across large coverage universes

**Objective:**  
Reduce analyst review time and surface key insights more efficiently by transforming raw transcripts into structured, decision-ready summaries and signals.

Potential benefits include:
- Faster post-earnings analysis
- More consistent interpretation of management commentary
- Early identification of tone shifts, risks, and emerging themes

---

## Data
The project uses publicly available earnings call transcripts sourced from:
- Motley Fool earnings call transcript dataset (Kaggle)

The dataset includes:
- Company identifiers
- Earnings call dates
- Speaker attribution (management, analysts)
- Full transcript text

> **Note:** Raw data files are intentionally excluded from the GitHub repository due to size constraints.

This project uses OpenAI’s API (e.g., for summarizing earnings call transcripts). To run the notebooks:
- Obtain an API key from OpenAI
- Set it as an environment variable in your system:

---

## Project Approach

### Phase 1: Data Loading & Cleaning
- Load and inspect raw transcript data
- Normalize text and handle formatting inconsistencies
- Identify key structural elements (company, date, speaker, content)
- Perform exploratory analysis on transcript length and coverage

### Phase 2: Earnings Call Summarization (Core Use Case)
- Generate concise summaries of earnings calls
- Focus on extractive summarization as a transparent baseline
- Produce analyst-friendly outputs such as:
  - Executive summary bullets
  - Key topics discussed
  - Management vs analyst emphasis
Metrics & Analysis 
- Added preliminary metrics to evaluate summaries:
- Character lengths, Word counts, Word compression ratios (summary length / original text length)
- Bullet counts
- Section presence counts for Prepared Remarks

These diagnostics uncovered instruction-following issues such as over-length summaries,repeated sections, and formatting drift.
It provides a foundation for prompt iteration and future semantic evaluation. 


### Phase 3: Sentiment & Tone Analysis (Extension)
- Apply sentiment analysis to management commentary
- Track tone changes across quarters
- Compare sentiment across companies or time periods

### Phase 4: Risk & Theme Detection (Future Work)
- Identify uncertainty and risk-related language
- Detect recurring vs emerging themes
- Analyze guidance language and hedging behavior

---

## Outputs
Planned outputs include:
- Structured earnings call summaries
- Sentiment scores and trends
- Topic and keyword analysis
- Visualizations supporting analyst review

---

## ROI and Use Cases
This pipeline is designed to support real-world investment workflows, including:
- Accelerating analyst post-earnings reviews
- Supporting portfolio managers with concise call insights
- Monitoring tone and risk language as part of fundamental analysis
- Scaling coverage without proportional increases in analyst headcount

---

## Repository Structure




