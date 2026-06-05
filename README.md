# Aspect-Based Sentiment Analysis of Shopee Consumer Reviews: A Case Study of Chocodot

## Overview

This repository contains the implementation of an Aspect-Based Sentiment Analysis (ABSA) model for analyzing consumer reviews of Chocodot products on Shopee. The study was conducted as an undergraduate thesis in the Digital Business program.

The objective of this research is not only to classify review sentiment, but also to identify specific product aspects discussed by consumers and analyze sentiment for each aspect. The findings are intended to support business decision-making by providing insights into consumer perceptions of Chocodot products.

## Research Background

Chocodot is a local chocolate brand from Garut, Indonesia, known for combining chocolate with traditional Garut dodol. Despite competing in a highly competitive chocolate market dominated by major brands, Chocodot has maintained its market presence for more than a decade.

Consumer reviews on e-commerce platforms contain valuable information regarding customer experiences and perceptions. Therefore, this study applies Aspect-Based Sentiment Analysis (ABSA) to identify which product aspects contribute to positive or negative consumer evaluations.

## Research Objectives

* Identify product aspects discussed in consumer reviews.
* Classify sentiment for each identified aspect.
* Analyze consumer perceptions toward Chocodot products.
* Generate business insights that may support product development and service improvement.

## Dataset

Source:
* Shopee product reviews

Period:
* 2020–2026

Products:
* Top 10 best-selling Chocodot products on Shopee

Initial dataset:
* 1,081 reviews

Final dataset:
* 1,014 valid reviews after filtering irrelevant reviews

Collected attributes:
* Username
* Rating
* Review date
* Review text

## Product Aspects

The analysis focuses on five predefined aspects:

1. Taste
2. Quality
3. Packaging
4. Price
5. Service

## Methodology

The research follows the CRISP-DM framework:

1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modeling
5. Evaluation
6. Deployment

### Data Preparation

Preprocessing steps include:

* Case folding
* Data cleaning
* Tokenization
* Text normalization
* Single-character removal
* Text reconstruction

### Aspect Detection

Aspect detection is performed using a keyword-based approach to identify the presence of predefined aspects within review texts.

### Sentiment Classification

Sentiment classification uses a fine-tuned IndoBERT model from the IndoBenchmark project.

Sentiment labels:

* Positive
* Negative
* Neutral

## Model

Base model:

`indobenchmark/indobert-base-p1`

Training configuration:

* Epochs: 3
* Batch size: 8
* Maximum sequence length: 128

## Model Access

Fine-tuned IndoBERT model:
https://huggingface.co/khoesan/ABSA-Chocodot

## Results

### Classification Performance

| Metric            | Score |
| ----------------- | ----- |
| Accuracy          | 0.90  |
| Weighted F1-Score | 0.88  |
| Macro F1-Score    | 0.66  |

Class-level performance:

| Class    | Precision | Recall | F1   |
| -------- | --------- | ------ | ---- |
| Positive | 0.91      | 0.99   | 0.95 |
| Negative | 0.79      | 0.65   | 0.71 |
| Neutral  | 1.00      | 0.18   | 0.31 |

### Business Insights

Key findings:

* Positive sentiment dominates the dataset (97%).
* Taste is the most frequently discussed aspect.
* Packaging, service, and quality receive the highest positive sentiment proportions.
* Taste and price exhibit more sentiment variation, indicating opportunities for improvement.

## Research Contribution

This study demonstrates how Aspect-Based Sentiment Analysis can be applied not only as a machine learning task but also as a business intelligence tool to understand customer perceptions and support strategic decision-making.

## Author

**Khoirotun Hisan**
Bachelor's Thesis Project
Digital Business Program
[Universitas Pendidikan Indonesia]

## Acknowledgements

This project was conducted as part of an undergraduate thesis under the supervision of:

- Rangga Gelar Guntara, S.Kom., M.Kom.
- Muhammad Rizki Nugraha, S.Pd., M.T.

## Citation

If you use this repository or reference this work, please cite:

```bibtex
@thesis{KhoirotunHisan2026,
  title={Aspect-Based Sentiment Analysis pada Ulasan Konsumen Shopee (Studi Kasus Chocodot)},
  author={Khoirotun Hisan},
  year={2026},
  school={[Universitas Pendidikan Indonesia]}
}
```
