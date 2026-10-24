# Transversal & Hitting-Set Solver

Find a transversal (vertex set intersecting every edge), one minimum transversal with transversal number τ(H), or enumerate minimal transversals. Results show selected vertices and the edge indices they hit; JSON export is available.

The algorithm exhaustively explores vertex subsets, with a 2,500,000-node budget and result limit. Worst-case exponential runtime; if a cap is reached, results may be incomplete. Minimal means inclusion-minimal; minimum means smallest cardinality.
