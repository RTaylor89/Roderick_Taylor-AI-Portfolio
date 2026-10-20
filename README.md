# Roderick Taylor - Applied AI Portfolio

## About Me

I am an Applied AI and Robotics student at Houston City College with an interest in practical natural language processing systems. This portfolio documents my work in text preprocessing, feature extraction, grammatical analysis, sentiment analysis, text classification, and named entity recognition.

My professional background shapes how I approach AI: I focus on reproducibility, responsible data handling, operational usefulness, and honest evaluation. I aim to build systems whose results people can inspect, understand, and use appropriately.

## Technical Skills

- **Languages and environments:** Python, Jupyter Notebook, VS Code, Google Colab
- **Text preprocessing:** HTML cleaning, contraction handling, tokenization, stop-word filtering, contextual lemmatization
- **Text representation:** TF-IDF, n-grams, vocabulary selection, feature interpretation
- **Linguistic analysis:** spaCy POS tagging, dependency parsing, rule-based relationship extraction, candidate semantic roles
- **Sentiment and emotion:** NLTK VADER, exploratory emotion lexicons, category-level sentiment analysis
- **Machine learning:** scikit-learn, Naive Bayes, Logistic Regression, support vector machines, cross-validation, hyperparameter search
- **Information extraction:** Named entity recognition, entity frequency analysis, co-occurrence mapping
- **Data and visualization:** pandas, NumPy, Matplotlib, Seaborn
- **Engineering practices:** Git, GitHub, dependency management, regression checks, documentation, training/test separation

## Featured Course

### Natural Language Processing - ITAI 2373

This course explores how computers process language, represent text numerically, analyze grammatical structure, identify sentiment, classify documents, and extract structured information. Course materials also introduce audio preprocessing and connections between text and speech analysis.

The NewsBot midterm combines the text-focused techniques into a working news intelligence pipeline.

| Project | Focus | Verified result |
|---|---|---|
| [NewsBot Intelligence System](https://github.com/RTaylor89/Roderick_Taylor-AI-Portfolio/tree/c24ee3895f56b50042d5013dc7637e6f5cde943f/ITAI2373-NewsBot-Midterm) | News classification, preprocessing, sentiment, POS, syntax, semantic-role candidates, and NER | Corrected SVM achieved **97.57% accuracy** and **0.9740 macro F1** on the existing 288-article test split |

The linked version is the repository snapshot cited in our group reflection.

## Featured Midterm Project

### NewsBot Intelligence System

**TeamLeemannTaylor — Roderick Taylor and Kate Leemann**

We built an integrated NLP prototype for news editors and media-monitoring analysts. Given an article, NewsBot suggests a category, extracts entity mentions, estimates textual sentiment, and returns linguistic patterns for human review.

The system integrates:

- Text cleaning, tokenization, stop-word filtering, and contextual lemmatization
- TF-IDF features and comparisons of vocabulary size, n-grams, and term-frequency scaling
- Naive Bayes, Logistic Regression, and SVM classification
- POS distributions, dependency features, and candidate semantic roles
- VADER sentiment and exploratory emotion-keyword analysis
- PERSON, ORG, GPE, DATE, and MONEY extraction
- Entity frequency and article-level co-occurrence analysis

### My Contributions

Kate and I contributed equally overall, with different responsibilities. I developed and reviewed code in VS Code, completed the correction pass, wrote eighteen regression checks, revised the technical report after review, and wrote the source reflection. Kate wrote the initial technical report and committed my updates.

Our shared work included duplicate removal, TF-IDF cross-validation, and cached spaCy processing. We adapted the instructor’s starter notebook through repeated exchanges and revisions. AI assistance supported implementation, debugging, and documentation.

### Collaboration and Version Control

We worked side by side, but our notebook copies drifted as I developed in VS Code and Kate moved between Colab and VS Code. Kate’s submitted copy lacked fixes present in my version.

This experience reinforced the importance of using one shared repository, committing frequently, and verifying the exact notebook version before submission. The submitted archive preserves the earlier state so later corrections remain traceable.

### Dataset and Evaluation

The BBC dataset contains 1,490 labeled articles. Removing 50 exact duplicate texts leaves 1,440 articles across Business, Entertainment, Politics, Sports, and Technology. A stratified split assigns 1,152 articles to training and 288 to testing.

TF-IDF fitting occurs within each training fold during three-fold cross-validation. Model selection uses macro F1 so each category receives equal weight.

The corrected SVM run achieved:

- **Accuracy:** 97.57%
- **Macro F1:** 0.9740
- **Technology recall:** 91.49%
- **Correct predictions:** 281 of 288

The corrected notebook completed all **27 code cells**, and **18 targeted regression checks** passed.

The existing test split had already informed error analysis. These results verify behavior on a known split; they do not establish independent improvement or performance on current news.

### Technical Lessons and Limitations

Adapting the starter required replacing assumptions about title, date, and source fields with the BBC dataset’s ArticleId, Text, and Category fields.

The correction pass addressed merged text boundaries, contractions, contextual lemmatization, and headline/body separation. Original text remains available for sentiment and grammatical analysis. Full notebook runs and targeted checks caught different kinds of failures.

Semantic analysis also exposed limits that successful execution alone cannot reveal. One rule labeled an instrument as a candidate agent. Entity aliases such as “Tony Blair” and “Blair” remained separate, and normalizing emotion keywords improved matching without validating the dictionary.

NewsBot could support article routing and mention discovery, but operational time savings remain unmeasured. Ambiguous topics, entity predictions, and sentiment estimates require human review. News sentiment does not establish public opinion or media bias.

## Documentation and Future Work

The project includes an executed notebook, analysis outputs, a technical report, a group reflective journal, dependency instructions, regression checks, and an archive of the submitted version.

Priorities for future development include:

- Independent evaluation on current news
- Near-duplicate detection before splitting data
- Human-labeled samples for sentiment, entities, and relationships
- Entity alias resolution
- Linguistic-feature comparisons using training-only cross-validation and an untouched final test set

## Portfolio Principles

- Include executable notebooks and inspectable results.
- Preserve submitted work and distinguish subsequent corrections.
- Document data sources, dependencies, and evaluation conditions.
- Report limitations alongside performance metrics.
- Keep raw datasets and full-article exports out of the public repository.
- Credit collaborators accurately and disclose AI assistance.
- Verify the exact version being published or submitted.

## Contact

- **Email:** [roderick.taylor@gmail.com](mailto:roderick.taylor@gmail.com)
- **LinkedIn:** [linkedin.com/in/rodjtaylor](https://www.linkedin.com/in/rodjtaylor/)
- **GitHub:** [github.com/RTaylor89](https://github.com/RTaylor89)
