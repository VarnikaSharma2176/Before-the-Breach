# Before the Breach
## Research Notes

## 1. Network Intrusion Detection

An Intrusion Detection System (IDS) monitors activity within a computing or communication environment and attempts to identify behaviour associated with security threats.

In a network-based IDS, network traffic or derived network-flow information can be analysed to distinguish legitimate traffic from malicious activity.

Machine learning provides a data-driven approach in which models can learn patterns associated with benign and malicious traffic from labelled or otherwise structured data.

---

## 2. Why This Is a Research Problem

At first glance, intrusion detection appears to be a straightforward classification problem:

> Given network traffic features, predict whether the traffic is benign or malicious.

However, the problem becomes more difficult when considering real-world conditions.

Important issues include:

- Multiple types of attacks may have very different characteristics.
- Attack classes may be highly imbalanced.
- Network behaviour changes over time.
- Dataset traffic may not fully represent operational networks.
- Features may contain redundancy or dataset-specific patterns.
- A model may perform extremely well on one dataset but generalize poorly.
- Accuracy alone may hide poor detection of minority attack classes.

A 2026 survey of 124 intrusion-detection datasets identified persistent concerns including limited real-world traffic representation, dataset bias, inconsistent documentation, evaluation risks, and underrepresentation of emerging attack vectors.

---

## 3. Dataset Quality Matters

The dataset is not simply a source of rows for training a model.

Its collection environment, attack scenarios, labelling process, feature representation, class distribution, temporal coverage, and realism can influence the conclusions drawn from an experiment.

Recent research has therefore emphasized systematic comparison and selection of IDS datasets rather than automatically selecting the most popular benchmark.

This will be an important principle when selecting our dataset.

---

## 4. Potential Dataset Families

### CIC-IDS2017

The Canadian Institute for Cybersecurity describes CIC-IDS2017 as containing benign traffic and common attacks, with both packet captures and labelled network-flow data. The dataset provides CSV files intended for machine-learning and deep-learning use.

Potential advantages:

- Widely used
- Labelled network flows
- Multiple attack scenarios
- Machine-learning-ready CSV data
- Official documentation available

Potential concerns to investigate:

- Dataset age
- Representativeness of the collection environment
- Class imbalance
- Dataset-specific patterns
- Generalization to other network environments

**Status:** Candidate only.

---

### TON_IoT

The UNSW TON_IoT dataset family was designed for cybersecurity research in IoT and Industrial IoT environments. It contains heterogeneous sources including telemetry, operating-system data, and network traffic collected in a Cyber Range and IoT laboratory environment.

Potential advantages:

- Modern IoT/IIoT context
- Heterogeneous data sources
- Cybersecurity-focused
- Suitable for machine-learning research

Potential concerns to investigate:

- Which subset is appropriate for our project?
- Whether its complexity is suitable for the INT234 scope
- How we would define the prediction target
- Whether the heterogeneous nature adds useful research value or unnecessary complexity

**Status:** Candidate only.

---

## 5. Initial Research Direction

The project should investigate more than which algorithm achieves the highest accuracy.

Potential investigation areas include:

- Model comparison
- Class imbalance
- Feature selection
- Feature scaling
- Dimensionality reduction
- Attack-class-specific performance
- False-positive and false-negative behaviour
- Generalization and evaluation methodology

The exact combination will be determined after dataset and literature analysis.

---

## 6. Important Research Principle

A high test score does not automatically mean that an intrusion-detection model is reliable.

The project should therefore examine:

> **What does the model's performance actually tell us, and what does it fail to tell us?**

This question should remain central throughout the research process.

## 7. Network Intrusion Detection Fundamentals

A network intrusion detection system (NIDS) monitors netword traffic and attempts to identify malicious or suspicious activity.

In a machine learning-based IDS, network traffic is represented using measurable features such as flow duration, packet counts, byte counts, packet length, protocol information, timing characteristics, and other traffic statistics.

The general predictive pipeline is: 
Network Traffic -> Features -> Preprocessing -> ML Model -> Predicted Class
## 8.Binary vs Multiclass Detection

Binary classification odentifies whether traffic is:
-Benign
-Malicious

Multiclass classification identifies the specific class of traffic, such as benign traffic or different attack categories.

Multiclass detection may provide greater research depth because models may perform differently across common and rare attacks.

## 9. Signature-Based vs Anomaly-Based Detection

Signature based detection identifies known attack patterns or signatures. It can be effective for known attacks but is limited when an attack does not match an existing signature.

Anomaly-based detection attempts to identify traffic that differs from expected behaviour. Machine learning can learn statistical patterns from historical traffic, although unusual legitimate traffic can also produce false positives.

## 10. Class Imbalance

Network intrusion datsets may contain substantially different number of records across traffic or attack classes.

A model trained on imbalanced data may favor majority classes and perform poorly on minority traffic or attack classes.

Therefore, high overall accuracy does not necessarily indicate reliable intrusion detection.

Relevant evaluation measures include:
-Precision
-Recall
-F1-score
-Confusion Matrix
-Class-wise performance
ROC-AUC where applicable

## 11. Dataset Variability and Generalization

Differnt intrusion datasets may differ in:
-Network environment
-Traffic characteristics
-Attack scenarios
-Feature dimensions
-Class distributions
-Data collection methodology

A model may therefore perform stronly on one dataset but differently on another dataset with different characteristics.

Generalization will therefore be considered during dataset and methodology selection.

## 12. Model Comparison Requirement

The project must implement and compare at least 4-5 suitable machine learning classification models.

The final model will be selected after considering:
-Dataset characteristics
-Research literature
-Model suitability
-Computational feasibility
-Relevance to the research question

The models will be evaluated under comaprable experimental conditions.

## 13. Current Research Consideration

The current investigation focuses on:
1. Class Imbalance
2. Data Preprocessing
3. Feature Representation
4. Dataset characteristics and variability
5. Model comparison
6. Class-wise Performance
7. Generalization where feasible

These are currently research considerationsrather than finalized experimental variables. The final methodology will be determined after dataset and literature investigation.