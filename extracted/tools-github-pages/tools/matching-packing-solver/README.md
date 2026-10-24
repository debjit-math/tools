# Matching & Packing Solver

A matching is a family of pairwise vertex-disjoint hyperedges. The tool can find one maximum matching (maximum cardinality) or enumerate maximal matchings (those to which no further edge can be added). Output includes the 1-based edge labels and JSON export.

The algorithm explores subsets with branch-and-bound for maximum matching and subset enumeration for maximal matchings. Worst-case exponential runtime; the search is capped at 3,000,000 nodes and maximal-matching output is capped by the selected limit. If a cap is reached, output may be incomplete.
