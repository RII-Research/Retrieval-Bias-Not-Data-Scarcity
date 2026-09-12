# Retrieval Bias and Epistemic Inequality in Retrieval-Augmented Generation

Reference implementation for the paper.

`Retrieval_Bias_Not_Data_Scarcity.ipynb` defines the generative model of the
retrieval-augmented generation pipeline and reproduces every experiment:

1. Main comparison of the fair and realistic operating points (Figure 1, Table 2)
2. Phase maps over the retriever-bias and representation planes (Figure 2)
3. Exact Shapley attribution of the North-South gap, with a construct ablation and a
   sensitivity sweep (Figure 3, Table)
4. Mitigation levers, including the deployable fair-exposure floor (Figure 4, Table 3)
5. Robustness to Northern prior imperfection (Table 4)
6. Retriever-bias calibration of four production embedders on FLORES-200 (Table 5)

Sections 1-5 are offline and seed-locked. Set `FAST = False` to reproduce the reported
numbers; `FAST = True` runs a coarser grid for quick inspection. Section 6 downloads
FLORES-200 and four sentence embedders and requires internet access; it runs on Google
Colab without modification. The notebook writes each figure to PNG and PDF.

## Requirements

Python 3.11. The offline sections require only `numpy` and `matplotlib`; the calibration
additionally requires `sentence-transformers`. See `requirements.txt`.

## Citation

Citation metadata is in `CITATION.cff`; GitHub's "Cite this repository" button generates
BibTeX and APA from it.
