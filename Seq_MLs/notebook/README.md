
---
# Fine-Tuning Notebooks for Protein Sequence Prediction
---

## `unirep_ACT.ipynb`

| Feature | Details |
|:--------|:--------|
| Model | UniRep (pretrained on UniRef50 dataset) |
| Architecture | LSTM |
| License | **Academic-only** |
| Fine-tuning method | Full fine-tuning |
| Input sequences | Evolutionary sequences gathered using BLAST searches |
| Output | Fine-tuned model for mutation activity prediction |

**UniRep** is used here primarily as a **baseline benchmark** for protein sequence mutation prediction.

---

## `protBert_ACT.ipynb`

| Feature | Details |
|:--------|:--------|
| Model | ProtBERT (pretrained on BFD dataset) |
| Architecture | Transformer (BERT) |
| License | Commercial use allowed |
| Fine-tuning method | Full fine-tuning |
| Input sequences | Evolutionary sequences obtained via BLAST |
| Output | Fine-tuned ProtBERT model capable of scoring mutant proteins |

 **ProtBERT** is modern, flexible, and optimized for production and commercial applications.

---

## Fine-Tuning Details (Both Notebooks)

- Evolutionary sequences are mined via **BLAST+**.
- Sequences are vectorized and fine-tuned fully.
- Mixed precision (`torch.amp.autocast`) is used for memory efficiency.
- 1 epoch, small batch size to fit Colab T4 GPUs (~16GB VRAM).

---

# Notes

- UniRep and ProtBERT have different licensing terms — make sure you understand which one to deploy based on your use case.
- Both models were designed to be production-ready in a future API server.

---

