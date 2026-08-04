# Cybersecurity Spend Record Matching using Text Processing and Fuzzy String Matching

This project presents an end-to-end product matching pipeline that identifies standardized cybersecurity products from noisy procurement spend records. The solution combines text preprocessing, exact string matching, and fuzzy string matching to accurately map procurement records to products in a master repository while generating confidence scores and explainable matching methods.

## Project Summary

Procurement records often contain typographical errors, abbreviations, inconsistent naming conventions, and multiple product mentions, making automated product identification challenging. This project addresses these issues by building a reproducible matching pipeline that standardizes text, performs exact and fuzzy matching, and enriches spend records with standardized product information.

## System Workflow

**Spend Records + Product Repository → Data Loading → Text Normalization → Exact Matching → Fuzzy Matching (RapidFuzz) → Confidence Scoring → Matched Records Export**

Each stage of the pipeline is designed to progressively reduce textual inconsistencies, improve matching accuracy, and produce transparent, reproducible results.

## Matching Methodology

The matching process follows a two-stage approach. Exact string matching is first used to identify direct product matches from normalized procurement text. When no exact match is found, RapidFuzz is used to identify similar product names based on string similarity.

Each matched record includes the product ID, product name, vendor name, confidence score, and the matching method used (Exact Match, Fuzzy Match, or No Match).

## Results

The pipeline successfully maps noisy procurement records to standardized cybersecurity products while preserving all original procurement data. The final output enriches each spend record with matched product information, confidence scores, and matching methods, providing an explainable and reproducible solution for procurement data analysis.

## Tech Stack

- Python
- Pandas
- Regular Expressions (re)
- RapidFuzz
- Jupyter Notebook
