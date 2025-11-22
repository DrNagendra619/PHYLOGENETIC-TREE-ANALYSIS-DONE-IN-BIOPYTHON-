# PHYLOGENETIC-TREE-ANALYSIS-DONE-IN-BIOPYTHON-
PHYLOGENETIC TREE ANALYSIS
# 🌳 Phylogenetic Tree Analysis using Biopython

## 📝 Overview

This repository contains a Jupyter Notebook (`phylogenetic tree analysis.ipynb`) dedicated to performing basic phylogenetic tree manipulation, visualization, and format conversion using the **Biopython** library, specifically its `Bio.Phylo` module.

The notebook demonstrates how to read phylogenetic trees from various file formats (Newick, PhyloXML), visualize them in both ASCII and graphical formats, modify tree properties (like rooting and clade colors), and convert between different tree formats (Newick, PhyloXML, NeXML, Nexus).

## 🚀 Project Steps & Demonstrations

The notebook executes a series of steps to demonstrate the capabilities of `Bio.Phylo`:

1.  **Installation**: Installs the necessary `biopython` library using `!pip install biopython`.
2.  **Tree Reading and Inspection (Newick)**:
    * Reads a sample phylogenetic tree from a file named **`simple.dnd`** (or similar Newick file) using `Phylo.read()`.
    * Prints the structure of the tree object.
    * Draws the tree structure in **ASCII format** using `Phylo.draw_ascii()`.
3.  **Graphical Visualization & Manipulation**:
    * Sets the tree as **rooted** (`tree.rooted = True`).
    * Draws the tree graphically using `Phylo.draw()`.
    * Converts the tree to a **PhyloXML** object for advanced metadata manipulation.
    * Colors the **root node** and a specific **Most Recent Common Ancestor (MRCA)** using PhyloXML properties.
    * Draws the final, colored, and rooted tree.
4.  **Format Conversion and Writing**:
    * Writes the tree object to the console in **PhyloXML** format using `Phylo.write()`.
    * Reads trees from a multi-tree **PhyloXML** file (`example.xml`).
    * Writes one tree (`tree1`) to a **Newick** file (`tree1.nwk`).
    * Uses `Phylo.convert()` to convert between:
        * Newick (`tree1.nwk`) to **NeXML** (`tree1.xml`).
        * PhyloXML (`other_trees.xml`) to **Nexus** (`other_trees.nex`).
5.  **Reading from String**: Demonstrates reading a Newick string directly from an `io.StringIO` object.
6.  **Visualization with Branch Lengths**: Reads a tree from a PhyloXML file and draws it with **branch lengths** displayed as labels.
7.  **External Program Execution (PHYLIP/PhyML)**: Executes a placeholder command (`/content/random.phy`) which suggests an attempt to run an external program (like PHYLIP or PhyML) for tree inference, and then reads and visualizes the resulting tree file (`random.phy_phyml_tree.txt`).

## 🛠️ Requirements and Setup

To run this notebook, you need:

* **Python**: Version 3.x
* **Jupyter Environment**: (e.g., JupyterLab, Jupyter Notebook, or Google Colab)

### Libraries

The core dependency is **Biopython**:

```bash
pip install biopython

Data Files

The script relies on several external data files, which must be present in the same working directory (or accessible via the specified path):

Filename,Format,Purpose
simple.dnd,Newick,Initial tree reading and visualization.
int_node_labels.nwk,Newick,Reading a more complex tree with internal node labels.
example.xml,PhyloXML,Demonstrating reading and parsing of a multi-tree PhyloXML file.
random.phy,PHYLIP (implied),Input for the external tree inference command.
random.phy_phyml_tree.txt,Newick,Output tree from the external inference command.

Usage Notes

    File Paths: The notebook uses hardcoded paths (e.g., "simple.dnd" or "/content/example.xml"). You must ensure these files are uploaded to your environment (like Google Colab) or correctly linked to your local working directory.

    External Programs: The execution of the cmd variable (/content/random.phy) assumes a file executable or shell command is available at that path, likely a command for a program like PhyML. This is a common pattern in bioinformatics notebooks.
