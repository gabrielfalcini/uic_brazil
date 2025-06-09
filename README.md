# uic_brazil
# University–Industry Collaboration in Brazil (OpenAlex)

This repository contains SQL queries used for a bibliometric analysis of university–industry collaboration publications in Brazil using OpenAlex.

## Contents
- SQL queries
- Explanation of query logic
- Project description

## Summary of Results (as of June 9)
- The query sample_creation selects Brazilian scientific articles published between 2012 and 2022 that include at least one Brazilian institution of type education and one of type company.
- The query returns 27,140 rows, representing 3,565 unique articles (each article may appear multiple times, once per institution).

- The query comparison_group_creation_v5 generates a comparison group highly similar to the UIC sample, but composed exclusively of articles without any collaboration between companies and educational institutions.
- Similarity is ensured by:
---- Matching the same year of publication as the paired UIC article;
---- Sharing at least one level-3 concept with the UIC article (with score > 0.7);
---- Requiring a strong thematic alignment, with an average score > 0.75 for shared concepts;
---- Including only articles (type = 'article');
---- Restricting to publications affiliated exclusively with Brazilian institutions.
- This query returns 56,786 rows, corresponding to 9,282 unique articles.
