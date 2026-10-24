# Hypergraph Isomorphism & Spectral Analyzer

A high-performance web-based tool for testing hypergraph isomorphism and computing spectral invariants. This tool is designed for discrete mathematicians and researchers who require an efficient, browser-based environment to analyze hypergraph structures.

### Key Features

* **Isomorphism Detection:** Utilizes vertex-signature pruning heuristics to quickly verify if two hypergraphs are isomorphic.
* **Spectral Analysis:** Implements the spectral adjacency matrix for hypergraphs, allowing for the comparison of spectral radii across hypergraph structures.
* **Flexible Input:** Supports both standard edge-set notation and binary incidence matrices.
* **Live Visualization:** Features an interactive bipartite graph representation using D3.js.
* **Non-Blocking Computation:** Heavy mathematical processing is offloaded to Web Workers to ensure a fluid user experience.

### Theoretical Foundation

The adjacency matrix $A_G = [(A_G)_{ij}]$ for a hypergraph $G = (V, E)$ is defined as:

$$(A_G)_{ij} = \sum_{e \in E_{ij}} \frac{1}{\vert{}e\vert{} - 1}$$

where $E_{ij} = \{e \in E : i, j \in e\}$.

For an $m$-uniform hypergraph, this simplifies to:

$$(A_G)_{ij} = d_{ij} \cdot \frac{1}{m - 1}$$

where $d_{ij}$ is the number of hyperedges containing both vertices $i$ and $j$. The degree of a vertex $i$ is calculated as:

$$d_i = \sum_{j=1}^{n} (A_G)_{ij}$$

### Reference

Banerjee, A. (2021). *On the spectrum of hypergraphs*. Linear Algebra and its Applications, 614, 82–110.

DOI: [10.1016/j.laa.2021.02.015](https://doi.org/10.1016/j.laa.2021.02.015)
