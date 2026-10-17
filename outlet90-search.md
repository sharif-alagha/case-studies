# Outlet90.com: Arabic and English product search

## Overview

[Outlet90.com](https://outlet90.com) is a WooCommerce store. Out of the box, WooCommerce search matches exact text, so misspellings, Arabic spelling variants and brand names written in different ways returned poor or empty results. I rebuilt the search so shoppers find what they mean, not only what they typed.

## My role

Designed, implemented and optimized the search experience, including database changes, relevance logic, caching, analytics and performance tuning.

## Stack

WooCommerce · WordPress · PHP · MySQL (full-text search, generated columns)

## What I built

### Search quality
- **Arabic normalization:** unifies common spelling variants of Arabic letters and removes diacritics so different spellings of the same word match.
- **Arabic phonetic search:** matches words that sound alike.
- **English phonetic and fuzzy matching:** tolerates typos and spelling variations.
- **Synonyms and dictionary support:** maps related terms to the same products.
- **Brand recognition:** detects brand names in the query, including different spellings, and uses them to narrow results.
- **Full-text search with relevance scoring:** ranks results by how well they match, not just whether they match.

### Performance and operations
- **Generated database columns** to precompute searchable and normalized text.
- **Search caching** to avoid repeating expensive queries.
- **Slow-query analysis and optimization** to find and fix the heaviest queries.
- **Performance optimizations** across the search path.
- **Analytics** on what shoppers search for, including searches that return nothing.

## How it works (high level)

<!-- TODO: edit this to match exactly what you built. -->

```
Shopper query
   → normalize (Arabic and English)
   → expand (synonyms, brand detection, phonetic keys)
   → match (full-text + fuzzy)
   → score and rank (relevance)
   → cache the result and log the query for analytics
```

## Results

<!-- TODO: add real numbers if you have them, for example:
- Searches with zero results: before X% → after Y%
- Average search response time: before X ms → after Y ms
- Catalog size (number of products) -->

[← Back to all case studies](README.md)
