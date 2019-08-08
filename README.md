# DpgMedia2019: A Dutch News Dataset for Partisanship Detection

## Citation

If you use this dataset, please cite the following paper:

```latex
@misc{1908.02322,
  Author = {Chia-Lun Yeh and Babak Loni and Mariëlle Hendriks and Henrike Reinhardt and Anne Schuth},
  Title = {DpgMedia2019: A Dutch News Dataset for Partisanship Detection},
  Year = {2019},
  Eprint = {arXiv:1908.02322},
}
```

## Description

This dataset consists of two levels of annotation of partisanship of Dutch news articles from DPG Media.
Detailed collection and annotation process can be found at URL

Short description of the files:

The first part was annotated on the publisher-level:
- dpgMedia2019-articles-bypublisher.jsonl: news articles (id, title, text, published_at)
  available at: https://partisan-news2019.s3-eu-west-1.amazonaws.com/dpgMedia2019-articles-bypublisher.jsonl
- dpgMedia2019-labels-bypublisher.jsonl: labels (id, partisan, publisher, url)

The second part was annotated on the article-level:
- dpgMedia2019-articles-byarticle.jsonl: news articles (id, title, text, published_at)
- dpgMedia2019-labels-byarticle.jsonl: labels derived from survey (id, partisan, publisher)


In addition, the raw survey data
- annotations.csv: 
  - RespondentId: unique to an annotator
  - ArticleId: unique to an article but only used internally in the survey
  - ExternalId: unique to an article and can be mapped to the id in jsonl files. Some articles have externalId marked 0, meaning that we could not find the article in the end.
  - Partisanship: please refer to the paper for detail
  - Polarity of partisanship: please refer to the paper for detail
  - Pro-, anti-: please refer to the paper for detail
- annotatorData.csv: 
  - RespondentId: unique to an annotator
  - Gender
  - Political_standpoint: answer to the question "Hoe zou u uw eigen politieke standpunt bepalen?"
  - Vote_for_party: answer to the question "Stel dat u binnenkort gaat stemmen, op welke partij gaat u dan stemmen?"
  
Finally, 
- dpgMedia2019-articles-byarticle-all.jsonl contains all articles that appeared in the survey so that if you want to compute new labels you have the articles


