# 🧬 Protein Activity Prediction Platform

Fine-tuning pretrained protein sequence models on evolutionary information for mutation activity prediction.

---

## 📦 Project Overview

This repository supports fine-tuning of:

- **UniRep** (LSTM, UniRef50 pretrained) – research-only.
- **ProtBERT** (Transformer, BFD pretrained) – commercially allowed.

Both workflows support full fine-tuning, inference, and experimentation for mutation prediction tasks.

---

## 📁 Repository Structure
```bash
Seq_MLs/
├── notebook/                   # Jupyter notebooks for exploration and training
│   ├── protBert_ACT.ipynb      # Fine-tuning & analysis
│   ├── unirep_ACT.ipynb        # Fine-tuning & analysis
│   └── README.md               # API usage instructions
├── prot_api_flask/            # 🧠 Flask API for mutation prediction
│   ├── prot_api_flask.py       # Single-file API server 
│   ├── sample_input.json       # Example input for curl/Postman 
│   └── README.md
└── README.md

Res_Int_Net/
├── notebook/
│   ├── prot_net_ligs_h.ipynb   # Graph-based residue-level network analysis
│   └── README.md
├── prot_api_flask/
│   ├── prot_api_flask.py       # Flask API for residue graph analysis
│   ├── residue_network.py      # Builds interaction graphs, computes centrality
│   ├── sample_input.json       # Example structure input
│   └── README.md               # API usage instructions
└── README.md

README.md
```

---

## 🚀 Flask Mutation Prediction API

A minimal REST API built with Flask to predict mutation effects based on a wild-type protein sequence and optional mutation data.

### 🔧 Run the API

`bash
pip install flask pandas
python prot_api_flask.py
API will run at:
http://127.0.0.1:5050/mutation_prediction

📡 Example Request
sample_input.json
json
Copy
Edit
{
  "wild_type_sequence": "MKTIIALSYIFCLVFADYKDDDDK",
  "mutation_csv_base64": null
}
Call with curl:
bash
Copy
Edit
curl -X POST http://127.0.0.1:5050/mutation_prediction \
  -H "Content-Type: application/json" \
  -d @sample_input.json
You may base64-encode a CSV file and replace "mutation_csv_base64" with that encoded string.

🛠️ Next Steps
Replace dummy predictions with real ProtBERT inference

Extend with additional models (e.g., ESM, ProteinMPNN)

Add model versioning, confidence scoring, and logging

Optional: containerize with Docker for deployment

📄 License
UniRep: Research-only.

ProtBERT: Commercial use allowed under Hugging Face license.

See individual model documentation for more details.
