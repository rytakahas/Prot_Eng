# 🧬 Prot_Eng: Protein Engineering Toolkit

**Prot_Eng** provides tools for protein structure and sequence-based analysis, supporting mutation effect prediction and residue interaction network exploration.

---

## 📚 Current Modules

### 1. 📂 Res_Int_Net
- **Residue Interaction Networks** (RINs) built from protein structures (PDB/AF2).
- Ligand and cofactor interactions are **weighted** by the number of **hydrogen bonds**.
- **Centrality metrics** (degree, closeness, betweenness) are calculated.
- 📓 Currently available as a **Jupyter Notebook**.
- 🛠️ API release planned soon!

### 2. 📂 Seq_MLs
- **Sequence-based Machine Learning models** for predicting mutation impacts.
- Fine-tuning of pretrained models like **UniRep** and **ProtBERT** on evolutionary sequence data.
- 📓 Currently available as **Jupyter Notebooks**.
- 🛠️ API release planned soon!

---

## 📬 Upcoming Developments

- ✅ **API for Res_Int_Net**:
  - Input: PDB ID or structure file.
  - Output: RIN graph with centrality scores.

- ✅ **API for Seq_MLs**:
  - Input: Protein sequence or mutant variants.
  - Output: Predicted activity or fitness scores.

- 🚀 **Combined API** (Future):
  - Jointly analyze sequence mutations **and** structure networks.
  - Enable holistic mutation effect prediction considering both sequence and 3D structural contexts.

---

## ⚡ Requirements

- Python 3.8+
- PyTorch
- HuggingFace Transformers
- Biopython
- NetworkX
- RDKit (optional for ligand analysis)

Install all dependencies:

```bash
pip install -r requirements.txt
```



