# Automorphism Group Explorer

Enumerates all vertex permutations preserving the hyperedge family, reports the automorphism group order, lists each automorphism as an image mapping, and computes vertex orbits. Duplicate edges are ignored as the input is treated as a set family. Isolated vertices are included if entered in the Vertices field.

Algorithm: backtracking over permutations, pruning candidates by vertex degree, then checking preservation of every edge. Worst-case factorial runtime; use small instances. Hard supported limit is 10 vertices.
