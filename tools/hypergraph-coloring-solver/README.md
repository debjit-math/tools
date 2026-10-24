# Hypergraph Coloring Solver

Supports weak coloring (every edge of size at least two must contain at least two colors) and strong coloring (each edge is rainbow). Includes a DSATUR-inspired vertex choice heuristic, bounded exact backtracking, optional search for the minimum color count up to a selected limit, color-class display, and JSON export.

Complexity is exponential in the worst case. The search has an assignment budget; reaching it is inconclusive. Singleton edges impose no weak-coloring constraint and trivially satisfy strong coloring.
