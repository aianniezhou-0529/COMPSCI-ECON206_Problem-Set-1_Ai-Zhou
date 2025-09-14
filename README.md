# COMPSCI-ECON206 Problem Set 1  
**Author:** Ai Zhou  
**Date:** September 2025  

---

## Abstract  
This project studies the one-round **Trust Game** through three disciplinary lenses:  
- **Economist**: theoretical derivation of Subgame Perfect Nash Equilibrium (SPNE).  
- **Computational Scientist**: replication of equilibrium results using NashPy (normal form) and GTE (extensive form).  
- **Behavioral Scientist**: empirical comparison between human play and an LLM (ChatGPT) session, with interviews and observations.  

We find that while SPNE predicts zero trust, both humans and the LLM sometimes deviate due to fairness, reciprocity, or framing. A new refinement — *Behavioral SPNE* — is proposed to incorporate social preferences and bounded rationality into extensive-form equilibrium analysis.

---

## Task Summary  
1. **Part 1 — Economist:**  
   - Defined Subgame Perfect Nash Equilibrium (SPNE).  
   - Proved existence using backward induction.  
   - Applied to Trust Game → equilibrium prediction: Player A invests 0, Player B returns 0.  
   - Welfare implications: equilibrium is inefficient compared to cooperative outcome.  

2. **Part 2 — Computational Scientist:**  
   - Built normal-form payoff matrices and solved with **NashPy** (Colab).  
   - Verified SPNE with **Game Theory Explorer (GTE)** in extensive form.  
   - Confirmed equivalence between SPNE (extensive form) and NE (normal form).  

3. **Part 3 — Behavioral Scientist:**  
   - Human experiment (oTree) showed deviations: positive transfers and returns motivated by fairness.  
   - LLM session revealed mixed strategies: fairness-based reasoning early, rational payoff-maximization later, sensitive to framing.  
   - Proposed **Behavioral SPNE**: equilibrium refinement with utility = monetary payoff + social preferences, and probabilistic choice via quantal response.  

---

## Key Figures & Tables  
- **Figure 1:** Payoff matrix (Word → PNG).  
- **Figure 2:** Nash equilibria computed with NashPy (Colab).  
- **Figure 3–5:** GTE extensive-form representation and solutions.  
- **Figure 6–8:** oTree human gameplay screenshots.  
- **Table 1:** Summary of Trust Game rounds (Human vs. LLM session).  

---

## Reproduction Steps  
1. Clone the repository:  
   ```bash
   git clone https://github.com/<your-username>/COMPSCI-ECON206_Problem-Set-1_Ai-Zhou.git
   cd COMPSCI-ECON206_Problem-Set-1_Ai-Zhou

