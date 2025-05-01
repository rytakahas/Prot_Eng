# 🧬 Protein Mutation Prediction Platform

Fine-tuning pretrained protein sequence models on evolutionary information for mutation activity prediction.

---

## Project Overview

This repository fine-tunes:

- **UniRep** (LSTM, UniRef50 pretrained) – research-only.
- **ProtBERT** (Transformer, BFD pretrained) – commercially allowed.

Both workflows enable full fine-tuning thanks to their manageable model size and flexible architecture.

---

## Planned + Implemented API (Flask)

I’ve implemented a minimal REST API using Flask for inference.

### Current Usage (Single-File API)

```bash
curl -X POST http://127.0.0.1:5050/mutation_prediction \
  -H "Content-Type: application/json" \
  -d @sample_input.json
```

Sample Input (sample_input.json)
```json
{
  "wild_type_sequence": "MKTIIALSYIFCLVFADYKDDDDK",
  "mutation_csv_base64": null
}
```

The API will return:

New mutant predictions

Fitness/activity scores

Metadata (CSV row count if provided)

### TODO List
- Build Flask-based API (prot_api_flask/)
- Add /mutation_prediction POST endpoint
- Implement Dockerfile for deployment
- Enable batch sequence input
- Add automated testing for API endpoints
- Add GPU-compatible ProtBERT loading via Hugging Face

### Directory Structure

```graphql
Seq_MLs/
├── notebook/protBert_ACT.ipynb # Jupyter notebooks for fine-tuning & analysis
├── notebook/unirep_ACT.ipynb # Jupyter notebooks for fine-tuning & analysis
├── prot_api_flask/           # Lightweight REST API for mutation prediction
│   ├── prot_api_flask.py     # Flask API (single-file)
│   ├── sample_input.json     # Example input for testing
│   └── README.md             # API documentation
├── README.md                 # Main project description (this file)
📄 License Information
Model	License	Usage
UniRep	Academic (non-commercial)	: Research Only
ProtBERT	Hugging Face (Apache 2.0)	: Commercial OK
```
### Requirements
- Python 3.8+
- PyTorch
- Hugging Face Transformers
- Biopython
- BLAST+
- Scikit-learn
- Flask (for API)

### Install all dependencies
```bash
pip install -r requirements.txt
```
  
### Notes
- UniRep: LSTM-based benchmark model. Not for production.
- ProtBERT: Transformer-based and commercial-friendly. Recommended for production APIs and deployments.
