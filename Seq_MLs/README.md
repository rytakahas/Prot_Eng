# 🧬 Protein Activity Prediction Platform

Fine-tuning pretrained protein sequence models on evolutionary information for mutation activity prediction.

---

## 📚 Project Overview

This repository fine-tunes:
- **UniRep** (LSTM, UniRef50 pretrained) – research-only.
- **ProtBERT** (Transformer, BFD pretrained) – commercially allowed.

Both workflows enable full fine-tuning thanks to their manageable model size.

---

## 📬 Planned API (Coming Soon)

### Example Usage:

```bash
curl -X POST http://127.0.0.1:5050/protein_sequence \
  -H "Content-Type: application/json" \
  -d @sample_request.json
```

The API will return:

New mutant sequences.

Predicted protein activities or fitness values.

✅ TODO List
 Build Flask-based API.

 Add /protein_sequence POST endpoint.

 Implement Dockerfile for deployment.

 Enable batch sequence input.

 Add automated testing for API endpoints.

📜 License Information

Model	License	Usage
UniRep	Academic (non-commercial)	❗ Research Only
ProtBERT	HuggingFace license (open)	✅ Commercial Friendly
⚡ Requirements
Python 3.8+

PyTorch

HuggingFace Transformers

Biopython

BLAST+

Scikit-learn

📦 Install all dependencies:

```bash
pip install -r requirements.txt
```


🧠 Notes
UniRep is a benchmark LSTM-based model.

ProtBERT is Transformer-based and ready for production deployments.

yaml
Copy
Edit

