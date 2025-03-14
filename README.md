### prot_seq_pred package structure

```
prot_seq_pred/
|
|── protein_act_pred/
│   ├── __init__.py
│   ├── data_preprocessing/
│   │   ├── __init__.py
│   │   ├── msa_processing.py
│   │   ├── blast_search.py
│   │   ├── jackhmmer.py
│   │   ├── mmseqs2.py
│   │   └── vectorization.py
│   ├── model_training/
│   │   ├── __init__.py
│   │   ├── regression.py
│   │   ├── classification.py
│   │   ├── xgboost_model.py
│   │   ├── cnn_model.py
│   │   └── lstm_model.py
│   ├── evaluation/
│   │   ├── __init__.py
│   │   ├── metrics.py
│   │   └── plot.py
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── file_utils.py
│   │   ├── sequence_utils.py
│   │   └── model_utils.py
│   └── main.py
├── notebooks/
│   └── notebook.ipynb
├── tests/
│   ├── test_msa_processing.py
│   ├── test_blast_search.py
│   ├── test_vectorization.py
│   ├── test_model_training.py
│   ├── test_metrics.py
│   └── test_utils.py
├── setup.py
├── requirements.txt
└── README.md
```
