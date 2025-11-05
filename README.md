[Hybrid Optimization of Therapeutic Targets in TNBC.md](https://github.com/user-attachments/files/23372880/Hybrid.Optimization.of.Therapeutic.Targets.in.TNBC.md)
# Hybrid Optimization of Therapeutic Targets in TNBC

This repository contains the source code for the computational methodology described in the article:

> **Hybrid Optimization of Therapeutic Targets in Triple-Negative Breast Cancer (TNBC) via Semidefinite Programming and Enhanced Boolean Simulation**
>
> *Authors: Sérgio Assunção Monteiro, Luís Alfredo Vidal de Carvalho, Fabricio Alves Barbosa da Silva*
>
> *[Journal to be inserted]*

The code implements a four-stage hybrid approach to identify optimal combinatorial therapeutic targets for the MDA-MB-231 cell line, focusing on the STAT3+BCL2 axis.

## 🚀 Reproduction of Results

The entire analysis, including the generation of all figures and the final ranking, can be reproduced by executing a single Python script.

### 1. Prerequisites

You need a working Python 3 environment. The following packages are required:

*   `networkx`
*   `cvxpy` (with a suitable solver like `clarabel` or `ECOS`)
*   `numpy`
*   `pandas`
*   `matplotlib`
*   `seaborn`

You can install all dependencies using `pip`:

```bash
pip install networkx cvxpy numpy pandas clarabel matplotlib seaborn
```

### 2. Project Structure

The repository contains the following files:

```
.
├── hybrid_optimizer.py   # Main script: Network Modeling, SDP, Boolean Simulation, Hybrid Analysis
├── plot_generator.py     # Module for generating all figures (Figures 1-9)
├── README.md             # This file
└── colab_hybrid_optimizer.py # Single-file version for Google Colab
```

### 3. Execution

Execute the main script from your terminal:

```bash
python3 hybrid_optimizer.py
```

The script will perform the entire analysis and generate the following output files in the execution directory:

#### Output Files

*   `hybrid_optimization_results.csv`: Final ranking of all gene pairs with their scores.
*   `gene_network_basic.png`: Basic gene regulatory network visualization.
*   `gene_network_targets.png`: Network with highlighted targets (STAT3+BCL2).
*   `gene_network_circular.png`: Circular layout of the network.
*   `ranking_pares.png`: Bar chart of the final ranking by Applicability Score.
*   `scatter_druggability.png`: Scatter plot of Druggability vs. Interaction Confidence.
*   `sensitivity_sdp_weights.png`: Sensitivity analysis for SDP weights.
*   `sensitivity_appl_weights.png`: Sensitivity analysis for Applicability Score weights.
*   `sensitivity_integration.png`: Sensitivity analysis for Integration weights.
*   `evolution_metrics.png`: Comparative analysis of methodological evolution.

## 💻 Google Colab / Jupyter Notebook

For easier execution without managing multiple files, use the single-file version:

1.  Open a new Google Colab notebook.
2.  Copy the entire content of the file `colab_hybrid_optimizer.py`.
3.  Paste it into a single cell and run.

The `colab_hybrid_optimizer.py` file includes an automatic dependency check and installation for the Colab environment.

## 📝 Citation

If you use this code or the methodology in your research, please cite the original article:

```
@article{monteiro2024hybrid,
  title={Hybrid Optimization of Therapeutic Targets in Triple-Negative Breast Cancer (TNBC) via Semidefinite Programming and Enhanced Boolean Simulation},
  author={Monteiro, Sérgio Assunção and Carvalho, Luís Alfredo Vidal de and Silva, Fabricio Alves Barbosa da},
  journal={[Journal to be inserted]},
  year={[Year to be inserted]},
  doi={[DOI to be inserted]}
}
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details. (Note: A LICENSE.md file is not included in this repository but is recommended.)
