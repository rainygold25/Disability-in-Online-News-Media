# Disability Media Bias Detection: Computational Sentiment Analysis

## Redefining Media Representation. Advancing Human-Centered AI

### Overview

This repository features the work from the UCSB SRA 2024 research track "Decoding Bias: Disability in Online News Media." It delivers a novel, production-grade pipeline to detect and quantify bias in global news coverage of disabilities using advanced Natural Language Processing (NLP) and statistical methods. Our solution leverages a two-stage Python system to extract, classify, and analyze thousands of news articles from the top 50 world media outlets, driving new insights into media-driven perceptions of human capability.


### Abstract

People with disabilities face persistent misrepresentation in mainstream media, influencing public perception and reinforcing historical stereotypes. This project designed and implemented a scalable architecture to answer two critical questions:
1. How does media representation of capability associate with sentiment in disability coverage?
2. Do portrayals differ between mental and physical disabilities?

Our findings reshape existing theories: negative sentiment dominates where incapability is implied; however, media bias does not systematically differ between mental and physical disabilities. The methodology and results empower future research, media accountability, and ethical AI development.

***

### Key Features

- **Full-Stack Data Pipeline:** 
  - Web scraping using Beautiful Soup for scalable article discovery.
  - Article parsing and NLP with Newspaper3k and NLTK for robust text extraction and tokenization.
  - Sentence-level capability and sentiment tagging via state-of-the-art spaCy POS tagging and VADER sentiment scoring.

- **Grammatical Role Classification:**
  - Subject = capable frame, object = incapable frame.
  - Algorithmically mapped using spaCy’s dependency parse trees.

- **Bias Quantification:**
  - Custom bias scores computed for each article: 
    $$
    \text{Bias Score} = \frac{\# \text{positive sentences} - \# \text{negative sentences}}{\text{total sentences}}
    $$
    - Supported by a rigorous chi-squared and two-sample T-test analysis for statistical soundness.

- **High-Impact Insights:**
  - Negative stereotypes persist where incapability is implied.
  - Capability frames yield higher positivity, with implications for AI and synthetic media fairness.
  - Framework generalizes to other bias domains—race, gender, socioeconomic status.

***

### Technical Implementation

- **Python 3.11**
- **Libraries:** Beautiful Soup, Newspaper3k, NLTK, spaCy, VADER, pandas, numpy, scipy
- Modular codebase includes:
  - `scraper.py`: Multi-threaded news link and article extractor
  - `analysis.py`: Text classification, sentiment scoring, and statistical analysis
  - `demo.ipynb`: Example pipeline run on representative sample dataset with full interpretability

***

### Results

- **Dataset:** >1,000 annotated articles; 10.7% used explicit capability frames.
- **Statistical Significance:** Capability framing is strongly linked to sentiment deviation (X², p < 0.05); bias scores for mental vs. physical disabilities statistically indistinguishable (t = 1.02, p = 0.31).
- **Replicability:** All code and methods are documented and reproducible—clone, run, and innovate for expanded applications.

***

### Impact

- Accelerates tech for social good by bringing transparency to media bias detection.
- Scalable and generalizable—deployable on any domain of media representation.
- Empowers ethical AI, supporting data-driven fairness in automated content moderation.

***

### Author Team

- Ranya Rajesh Prasad (Keyword Engineering, Pipeline Design and Optimization)
- Isabella Bian (Lead Developer, Architecture)
- Jiyoon Stella Lee (Sentiment Analysis, Statistical Validation)

- Mentored by Professor Musa Malik and the UCSB SRA Summer Research Academies

***

### Citation

If leveraging this repo for research, please cite as:
> UCSB SRA 2024 Disability Media Bias: Computational Analysis of Capability and Visibility Effects.

***

For recruiters who believe in the power of AI to reshape perceptions and systems—this repository exemplifies innovation, impact, and practical vision.

