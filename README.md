# Transparency-EMNLP
This is the GitHub page containing the data for the paper "Linking Transparency and Accountability: Analysing The Connection Between TikTok's Terms of Service and Moderation Decisions"


- **/data: Policy corpus (chunked)**  TikTok’s public-facing rules combined from five document families: **Terms of Service**, **Community Guidelines**, **Advertising Policies**, **Brand Guidelines**, and **Commercial Terms**. The corpus is segmented into **124** clause-level “chunks” used as retrieval targets. See Chunked_Guidelines_reworked.csv.
- **/Gold_data_cleaned: TikTok-100 (gold annotations)** A gold-standard set of **100** SoRs, each **independently annotated by two legal research assistants**. For every SoR, annotators (i) selected the best-matching policy chunk(s) from the 124-chunk corpus and (ii) rated five clarity dimensions: **Clarity, Understanding, Unclear Terms, Detail Level** (1–4 scales) and **Redress clarity** (binary). The guidelines for these clarity dimensions can be seen under /annotations/Required_Annotations.pdf. The /collapsed_datasets contain analysis-ready CSVs that slice the gold data by dimension (e.g., `clarity_dataset.csv`, `redress_dataset.csv`, etc.).
- **/annotations: Annotation guide** As mentioned before, these are the guidelines for the clarity dimension labelling.
- **sample_100.parquet:** This is a collection of 100 unique, random SoRs that were given to the annotators to label and later used for analysing and evaluating the models.

Structure tree:
<pre>
GitHub_code/
├── annotations/
│   └── Required_Annotations.pdf <- File used by the legal research assistant team to annotate the sample set
├── data/
│   ├── Advertisement_Policies/
│   │   ├── tiktok_policy_text.txt <- TikToks policy text
│   │   ├── tiktok_policy_text_deduplicated.txt <- Same text but duplicates removed
│   │   ├── tiktok_policy_text_filtered.txt <- Same text but filtered
│   │   └── tiktok_policy_text_relevant.txt <- The remaining relevant parts of the policy text
│   ├── community_guidelines/
│   │   ├── Brand Guidelines.md
│   │   ├── Commercial Terms.md
│   │   ├── Community Guidelines.md
│   │   └── Terms of Service.md
│   ├── ToS/
│   │   ├── tiktok_entries_claudette.csv <- The files by the CLAUDETTE team for TikTok containing their labels
│   │── Chunked_Guidelines_reworked.csv <- The combined guidelines segmented into 124 chunks.
│   └── Gold_data_cleaned/
│       ├── collapsed_datasets/ <- Binarised files for each clarity dimension for training the classifiers
│       │   ├── clarity_dataset.csv
│       │   ├── combined_clarity_questions.csv <- The combined CSV of all the other files in this folder
│       │   ├── detail_level_dataset.csv
│       │   ├── redress_dataset.csv
│       │   ├── unclear_terms_dataset.csv
│       │   └── understanding_dataset.csv
│       ├── Gold_data_for_analysis.csv <- The combination of the best picked chunks of both annotators, containing uuid, the SoR, label of annotator 1, label of annotator 2
│       ├── law_1.csv <- Individual labels from the four legal research assistants  
│       ├── law_2.csv
│       ├── law_3.csv
│       ├── law_4.csv
│       └── sample_100.parquet <- The 100 random SoRs that were given to the team of assistants
└── README.md <- This README
</pre>

