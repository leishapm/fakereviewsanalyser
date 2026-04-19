##  Fake Reviews Analyzer  
### Cross-Domain Detection of Deceptive Online Reviews  

**SC3021 Data Science Fundamentals Project**

---

###  Team  
- Harshini Mahalingam  
- Leisha Pritika Menezes  
- Nandit Ramesh  

---

##  Overview  

Online reviews play a major role in shaping consumer decisions, but a significant portion of them are fake, incentivised, or AI-generated. With the rise of large language models, generating realistic reviews has become easier than ever, making detection increasingly challenging.

This project builds a **fake review detection pipeline** that goes beyond standard single-domain evaluation. Instead of training and testing on similar datasets, we deliberately train on one domain and evaluate on entirely different domains to simulate real-world deployment conditions.

---

##  Objective  

To investigate whether **linguistic patterns of deception generalise across domains**, and to evaluate how effectively machine learning models can detect fake reviews when exposed to unseen data distributions.

---

##  Key Idea  

Most fake review detection systems are evaluated on the same domain they were trained on, which often leads to inflated performance.

This project adopts a cross-domain approach:

- Train on:
  - Product reviews  
  - Hotel reviews  

- Evaluate on:
  - App reviews  
  - Unseen hotel reviews  

This forces the model to rely on **generalisable deception signals** rather than dataset-specific patterns.

---

##  Project Pipeline  

| Stage | Description |
|------|------------|
| **Ask** | Define the research question and hypothesis |
| **Prepare** | Load datasets and identify sources |
| **Profile** | Assess structure, quality, and label availability |
| **Enrich** | Extract linguistic and stylistic features |
| **Clean** | Preprocess and standardise text |
| **Structure** | Unify schema across datasets |
| **Analyse** | Perform exploratory and diagnostic analysis |
| **Model** | Train hybrid deep learning model |
| **Predict** | Conduct cross-domain evaluation |

---

##  Datasets  

- **DS1 – Fake Reviews Dataset (Kaggle)**  
  Product domain with 20k genuine and 20k AI-generated reviews  

- **DS2 – Deceptive Opinion Spam Corpus**  
  Hotel domain with controlled human-written deceptive and truthful reviews  

- **DS3 – Google Play Store Reviews**  
  App domain, unlabelled, used for cross-domain evaluation  

- **DS4 – TripAdvisor Hotel Reviews**  
  Hotel domain, unlabelled, used for cross-domain evaluation  

---
##  Dataset Access  

The datasets used in this project are hosted externally due to size constraints.

Google Drive Link:  
https://drive.google.com/drive/folders/1GCCONZDA_wSQUIP19BzCYLWu-ynJzxbE?usp=drive_link

### Instructions  
1. Open the link  
2. Make a copy to your own Google Drive  
3. Ensure the folder structure and file names remain unchanged  
4. Update dataset paths in the notebook if required

---
### Expected Structure  
```
SC3021Notebook/
└── SC3021Notebook/
├── nltk_data/
├── fake_reviews_dataset.csv
├── deceptive-opinion.csv
├── tripadvisor_hotel_reviews.csv
├── google_play_store_reviews.csv
```

### Note  
Ensure you are using the **inner folder** containing the dataset files. Incorrect paths will cause the code to fail.

---
##  Model Approach  

This project uses a **hybrid model** combining deep learning with engineered features:

###  Bidirectional LSTM (BiLSTM)
- Captures contextual and sequential patterns in text  
- Learns dependencies in both forward and backward directions  

###  Engineered Features
- Sentiment polarity  
- Review length  
- Lexical diversity  
- Frequency of exaggerated or emotional language  

This hybrid approach improves robustness by combining representation learning with interpretable signals.

---

##  Key Contributions  

- Cross-domain evaluation instead of single-domain benchmarking  
- Integration of deep learning and linguistic feature engineering  
- Realistic testing setup that reflects deployment scenarios  
- Analysis of how well deception signals transfer across domains  

---

##  Expected Outcomes  

- Insights into the generalisability of fake review detection models  
- Evaluation of hybrid model performance on unseen domains  
- Identification of limitations in current detection approaches  

---

##  Conclusion  

This project highlights a critical gap in fake review detection: models that perform well in controlled settings often fail in real-world scenarios.

By focusing on cross-domain evaluation, this work aims to move toward **more reliable and deployable detection systems**.
