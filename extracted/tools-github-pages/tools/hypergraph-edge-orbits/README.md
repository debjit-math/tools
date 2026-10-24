# Hypergraph Edge Orbits — Code Analysis

## Purpose
This standalone browser tool accepts a finite hypergraph (as a list of edges) and a permutation of its vertices. It computes successive images of each edge under that permutation, displays an orbit table, and visualizes the edge-orbit structure as an interactive graph.

## Inputs
- **Edge sets:** Enter edges using braces or plain comma-separated vertices. Edges can be separated by commas outside braces, semicolons, or new lines. Example: `{1,2}, {2,3}, {1,3}`.
- **Permutation:** Accepts cycle notation such as `(1 2 3)` (including multiple disjoint cycles) or mapping notation such as `1→2, 2→3, 3→1`.
- The permutation must be a bijection on the specified mapping domain. Every vertex used in an edge must have an image specified; fixed points should be explicit in mapping notation.

## Computation
1. `parseEdges` tokenizes edge sets while respecting braces and removes repeated vertices within an edge.
2. `parsePermutation` builds a vertex-to-image map from cycle or mapping notation and validates one-to-one mappings and completeness of the mapping domain.
3. `applyPermutation` maps each vertex in an edge and sorts the resulting vertices.
4. `orbitFor` repeatedly applies the permutation until an edge repeats, producing the orbit of that edge.
5. The table shows the successive images `σ^k(E_i)`. The number of rows is the maximum orbit length among the entered edges. Input edges are labeled from 1 (`E1`, `E2`, …); the first row is `k = 0`, representing the original edge.

## Visualization
The SVG edge-orbit graph represents each input edge as a node. Nodes in the same orbit share a color, and every pair of nodes in the same orbit is connected. Users can drag nodes, zoom in/out, reset the layout, and toggle edge labels. The graph includes a legend summarizing orbit sizes.

## Dependencies
- HTML, CSS, and JavaScript run in the browser.
- MathJax 3 is loaded from jsDelivr to typeset mathematical notation. Internet access is needed for MathJax; the computation itself is implemented locally in JavaScript.

## Notes and limitations
- The tool is a single HTML file and does not require a build step or server-side runtime.
- Orbit calculation stops when an edge already seen in the orbit is encountered. This is appropriate for a permutation acting on a finite edge set.
- The parser accepts vertex identifiers as text, but permutation mappings must cover every vertex appearing in the input edges.
- This README describes the behavior visible in the supplied source; it does not independently certify mathematical correctness for every possible input.
