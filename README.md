# nlp-welfare-guidance-complexity
# Lost in the System: An NLP Analysis of Linguistic Complexity in UK Welfare Guidance for Refugees and Asylum Seekers

MSc AI and Sustainable Development Dissertation, University of Birmingham (2026)

## Overview

This repository contains the code and data for a study measuring linguistic complexity across three tiers of UK welfare benefits guidance: central government (GOV.UK), local councils, and third sector organisations. The study focuses on guidance relating to refugee and asylum seeker welfare support as a case study for examining broader patterns in how welfare guidance is written and delivered.

## Research Questions

1. How does linguistic complexity vary across central government, local council, and third sector benefits guidance?
2. Which dimensions of complexity are most prevalent, and do they differ by tier and theme?
3. Can automated readability features reliably predict human-assessed complexity?

## Repository Contents

- `analysis_notebook.ipynb` — Full analysis pipeline including data preprocessing, feature extraction, annotation analysis, classification (Random Forest, SVM, Logistic Regression), and visualisations
- `Master_Annotation_File.csv` — Annotated corpus of 348 paragraphs with complexity labels (1-3), tier, theme, and source metadata


## Method Summary

- **Corpus**: 348 paragraphs (86 central government, 111 local councils, 151 third sector)
- **Annotation**: Manual 3-point complexity scale across four dimensions (lexical, syntactic, cohesion, navigational)
- **Automated features**: 10 features including Flesch-Kincaid, Dale-Chall, jargon density, passive voice percentage, average sentence length, word count, average word length, long word percentage, noun phrase count, and sentence length variability
- **Classification**: Random Forest (best performer, 60% accuracy, 0.51 F1), SVM, Logistic Regression

## Key Findings

- Central government guidance was the most complex despite a plain language mandate; local councils were the most accessible
- Third sector organisations simplify effectively for housing but were more complex than central government on financial support
- Jargon density was the strongest predictor of human-assessed complexity; Flesch-Kincaid scores could not distinguish accessible from inaccessible guidance

## Requirements

The analysis was run in Google Colab using Python. Key libraries include pandas, scikit-learn, nltk, textstat, matplotlib, and seaborn.

## Author

Amira Al-Shereidah, University of Birmingham
