# Graph Dataset Exploration

Exploratory data analysis and visualization of three widely used **graph-classification benchmark datasets** — **NCI1**, **PROTEINS**, and **MUTAG** — loaded from PyTorch Geometric's TUDataset collection. Rather than training a model, this notebook characterises each dataset: how large the graphs are, how many graphs there are, and how the classes are balanced, so the datasets can be compared side by side before any modelling.

> **Note on scope:** This is an exploratory/analysis notebook — it inspects and visualizes datasets; it does not train or evaluate any model.

## Datasets

All three are standard molecular / bioinformatics graph-classification benchmarks, downloaded automatically by PyTorch Geometric (`TUDataset`) with `NormalizeFeatures` applied:

| Dataset | Domain | Task |
|---------|--------|------|
| **NCI1** | Chemical compounds | Activity against non-small-cell lung cancer |
| **PROTEINS** | Proteins | Enzyme vs. non-enzyme |
| **MUTAG** | Nitroaromatic compounds | Mutagenicity |

Each graph has node features and a single graph-level class label.

## What the notebook does

For every dataset it computes, per graph, the number of nodes and edges, the total number of graphs, and the class distribution, then visualizes them several ways for comparison:

- **Histograms** of node and edge counts
- **Class-distribution** bar charts
- **Box plots** and **violin plots** of node/edge counts across datasets
- **Strip plots** with a custom palette
- **Bar and pie charts** of total graph counts per dataset

The datasets download to `/tmp` at runtime, so nothing needs to be committed to the repository.

## Requirements

Developed in Google Colab. Main dependencies:

- `torch`
- `torch_geometric`
- `numpy`
- `matplotlib`
- `seaborn`

Install everything with:

```bash
pip install -r requirements.txt
```

## Getting started

1. Open the notebook in Google Colab or Jupyter.
2. Run the cells top to bottom — the TUDatasets are fetched automatically on first use.
3. Each cell produces a different comparative visualization of the three datasets.

## Repository structure

```
.
├── Datasets_Graph.ipynb
└── README.md
```
