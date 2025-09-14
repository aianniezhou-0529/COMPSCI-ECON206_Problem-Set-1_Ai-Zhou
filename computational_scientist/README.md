# Computational Scientist Component

This folder contains the computational implementation and analysis of the Trust Game.

## Contents
- `notebook.ipynb`: A Colab-exported Jupyter notebook with:
  - Construction of discretized payoff matrices (Investor strategies × Trustee return rates).
  - Computation of Nash equilibria using [NashPy](https://nashpy.readthedocs.io/).
  - Backward induction analysis and identification of Subgame Perfect Nash Equilibrium (SPNE).
  - Export of equilibria results (`nash_equilibria.json`, CSVs of payoff matrices).
- `gte/` (optional): Exports from Game Theory Explorer (GTE) if used.
- `screenshots/`: Screenshots of the GTE game tree and/or equilibrium solutions.

## How to Run
1. Open the notebook in [Google Colab](https://colab.research.google.com/).
2. Install dependencies inside the notebook:
   ```bash
   !pip install nashpy matplotlib pandas
3. Run all cells.
   Outputs include payoff matrices, computed equilibria, and JSON/CSV files in the computational_outputs/ folder.

## Example Outputs

Payoff matrices for Investor (A) and Trustee (B).

Nash equilibria (pure/mixed) in JSON format:

[
  {
    "A_strategy_probs": [1.0, 0.0, 0.0],
    "B_strategy_probs": [1.0, 0.0, 0.0],
    "A_expected_payoff": 100.0,
    "B_expected_payoff": 0.0
  }
]


SPNE analysis: Identified by backward induction.
In the discretized trust game, the SPNE corresponds to:

Trustee (B) returning nothing (r = 0) in every subgame.

Investor (A) anticipating this, choosing not to invest (x = 0).

## Notes

Discretization: A’s strategy space {0, 50, 100}, B’s return rates {0%, 50%, 100%}.

Larger grids possible but lead to exponential growth in state space.

The computational analysis complements the economist’s theoretical section and the behavioral scientist’s experiments.

## References

Shoham, Y., & Leyton-Brown, K. (2009). Multiagent Systems: Algorithmic, Game-Theoretic, and Logical Foundations. Cambridge University Press.

NashPy documentation: https://nashpy.readthedocs.io/

Game Theory Explorer (GTE): http://gte.csc.liv.ac.uk/
