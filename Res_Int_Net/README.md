# 🧬 Res_Int_Net: Residue Interaction Network Analysis

This project builds **Residue Interaction Networks (RINs)** from protein structures, incorporating **ligands** and **cofactors** as weighted nodes based on the number of hydrogen bonds.

The pipeline can accept:
- **Experimental structures** (PDB IDs)
- **Predicted models** (e.g., AlphaFold2, ESMFold)

---

## 📚 Project Overview

- Parse protein 3D structures.
- Construct a graph where nodes = residues/ligands, edges = interactions.
- Ligand and cofactor connections are **weighted** by the number of **hydrogen bonds**.
- Calculate **centrality measures** (degree, closeness, betweenness) for each node.
- Analyze the impact of ligands/cofactors on the structural network.

---

## 📬 Planned API (Coming Soon)

### Example Request

```bash
curl -X POST http://127.0.0.1:5050/analyze_structure \
  -H "Content-Type: application/json" \
  -d @sample_request.json

Input: JSON containing either:

A PDB ID (download automatically).

A file path to a local structure (PDB/mmCIF format).

Output: RIN graph metrics and centrality scores.

✅ TODO List
 Implement Flask API server.

 Accept either PDB ID or uploaded structure file.

 Build RIN graph dynamically with ligand interactions.

 Return JSON with centrality results and graph summaries.

 Dockerize for easy deployment.

⚡ Requirements
Python 3.8+

Biopython

NetworkX

RDKit (optional, for more advanced ligand handling)

Matplotlib / Seaborn (optional for plotting)

Install with:

bash
Copy
Edit
pip install -r requirements.txt
🧠 Notes
Ligand weights enrich the standard RIN approach by capturing chemical environment effects.

This approach is suitable for small molecule docking evaluations, druggability assessments, and protein design tasks.
