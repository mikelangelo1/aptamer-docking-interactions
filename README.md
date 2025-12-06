# Protein-DNA Docking Analysis

A comprehensive Python pipeline for analyzing protein-DNA/RNA aptamer interactions from HADDOCK docking results using ProLIF and MDAnalysis.

## 🚀 Features

- **Automated Interaction Analysis**: Detect 9+ interaction types (H-bonds, hydrophobic, π-stacking, ionic, etc.)
- **Multi-Cluster Support**: Process and compare HADDOCK docking clusters
- **DNA/RNA Compatible**: Works with both DNA and RNA aptamers
- **Visualization**: 2D/3D molecular visualization with py3Dmol and Plotly
- **Residue-Level Insights**: Identify key interacting residues and contact frequencies

## 📦 Installation

```bash
pip install prolif MDAnalysis matplotlib seaborn plotly py3Dmol networkx pandas numpy rdkit
```

## 🔧 Quick Start

1. **Organize your HADDOCK results** (cluster*.pdb files)
2. **Run the analysis notebook**:
```python
# Configure your results directory
RESULTS_DIR = Path("/path/to/your/haddock/results")
```
3. **Execute the cells** to:
   - Load and prepare structures
   - Calculate interactions
   - Generate visualizations
   - Export results

## 📊 Output

- **Interaction statistics** by cluster and pose
- **Most frequent residue pairs** with distances
- **Publication-ready plots** (PNG/PDF)
- **DataFrames** for further analysis

## 🧪 Example Analysis

```python
# Analyze a single docking pose
result = comprehensive_interaction_analysis("cluster10_1.pdb")
print(f"Total interactions: {result['total_interactions']}")
print(f"Nucleic acid type: {result['nucleic_type']}")
```

## 📁 Structure

```
docking-interaction.ipynb  # Main analysis notebook
results/                   # HADDOCK output PDBs
output/                    # Generated analysis files
```

## 📚 Dependencies

- **ProLIF 2.0+**: Molecular interaction fingerprints
- **MDAnalysis**: Structure analysis
- **RDKit**: Chemical informatics
- **Plotly/py3Dmol**: Visualization

## 🤝 Contributing

Contributions welcome! Please feel free to submit a Pull Request.

## 📄 License

MIT License - see LICENSE file for details.

## 🙏 Acknowledgments

- ProLIF developers for interaction fingerprinting
- MDAnalysis team for structural analysis tools
- HADDOCK developers for molecular docking software