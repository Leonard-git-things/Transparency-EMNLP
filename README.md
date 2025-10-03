# Transparency-EMNLP
This is the GitHub page containing the data for the paper "Linking Transparency and Accountability: Analysing The Connection Between TikTok's Terms of Service and Moderation Decisions"


- **/data: Policy corpus (chunked)**  TikTok’s public-facing rules combined from five document families: **Terms of Service**, **Community Guidelines**, **Advertising Policies**, **Brand Guidelines**, and **Commercial Terms**. The corpus is segmented into **124** clause-level “chunks” used as retrieval targets, which is under the file Chunked_Guidelines_reworked.csv.
- **/Gold_data_cleaned: TikTok-100 (gold annotations)** A gold-standard set of **100** SoRs, each **independently annotated by two legal research assistants**. For every SoR, annotators (i) selected the best-matching policy chunk(s) from the 124-chunk corpus and (ii) rated five clarity dimensions: **Clarity, Understanding, Unclear Terms, Detail Level** (1–4 scales) and **Redress clarity** (binary). The guidelines for these clarity dimensions can be seen under /annotations/Required_Annotations.pdf. The /collapsed_datasets contain analysis-ready CSVs that slice the gold data by dimension (e.g., `clarity_dataset.csv`, `redress_dataset.csv`, etc.).
- **/annotations: Annotation guide** As mentioned before, these are the guidelines for the clarity dimension labelling.
- **sample_100.parquet:** This is a collection of 100 unique, random SoRs that were given to the annotators to label and later used for analysing and evaluating the models. 

