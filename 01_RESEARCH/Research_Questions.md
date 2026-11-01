# Before the Breach
## Research Questions

### 1. Broad Research Problem

Modern networks generate large volumes of traffic that may contain both legitimate activity and malicious behaviour. Intrusion Detection Systems attempt to identify suspicious activity, but machine-learning-based IDS models can be strongly affected by the characteristics of the training data, feature representation, class distribution, and evaluation methodology.

The project will investigate the use of machine learning for network intrusion detection and determine which factors most strongly influence the reliability of the resulting predictions.

---

## 2. Primary Working Research Question

> **How reliably can machine learning models detect and classify network intrusions, and how do data and modelling choices affect their performance?**

This question is provisional and will be refined after the dataset and existing literature have been studied.

---

## 3. Secondary Research Questions

### Dataset

- What characteristics make an intrusion-detection dataset suitable for machine-learning research?
- How representative is the selected dataset of realistic network behaviour?
- What attack categories and benign traffic are represented?
- How balanced are the classes?

### Data Preparation

- How does preprocessing affect intrusion-detection performance?
- Which features require scaling or transformation?
- Are there redundant or irrelevant features?
- Can dimensionality reduction preserve useful information?

### Machine Learning

- Which supervised learning algorithms are suitable for intrusion detection?
- How do different models compare in detecting different attack categories?
- Which models provide the best balance between detection performance and false alarms?

### Evaluation

- Is accuracy sufficient for evaluating an intrusion-detection model?
- How do precision, recall, F1-score and confusion matrices change the interpretation of model performance?
- Which attack classes are most difficult to detect?
- How does class imbalance influence evaluation results?

### Research Reliability

- Could a model achieve high performance because of characteristics specific to the dataset rather than because it has learned generalizable attack patterns?
- How can the evaluation methodology reduce misleading results?
- What limitations of the dataset should be considered when interpreting the findings?

---

## 4. Questions to Investigate Through Literature Review

- What are the major approaches to network intrusion detection?
- How have machine-learning models been used for IDS?
- Which datasets are most frequently used?
- What limitations have researchers identified in existing IDS datasets?
- What evaluation practices are considered reliable?
- What research gaps remain relevant to a student-scale but technically meaningful study?

---

## 5. Final Research Question

**Status:** Not finalized.

The final research question will be selected only after:

1. Dataset investigation
2. Literature review
3. Research-gap analysis
4. Feasibility assessment

This is intentional. The project should be driven by an evidence-based research question rather than choosing a question first and forcing the dataset and methodology to fit it.