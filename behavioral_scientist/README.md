# Behavioral Scientist Component

This folder contains the behavioral and AI-based experimental analysis of the Trust Game.

## Contents
- `otree_app.zip`: A ready-to-run oTree app for the one-round Trust Game.
- `screenshots/`: Screenshots of game instructions, decision screens, and results pages.
- `llm/`: Contains LLM session materials:
  - `prompts.txt`: Exact prompts used for ChatGPT during the game.
  - `transcript.md`: Session transcripts with investments, returns, and reasoning.
  - `settings.json`: Any special LLM configuration (temperature, model version, etc.).
- `README.md`: This file.

## oTree Deployment
1. Unzip `otree_app.zip`.
2. Follow standard oTree installation instructions: <https://otree.org/>.
3. Run locally or deploy on a server.
4. Configure session with two participants.
5. Collect choices, payoffs, and post-play interviews.
6. Record observations in tables and summary notes.

### Observations from Human Session
- Player A invested a moderate amount, showing some trust.
- Player B returned roughly one third of the multiplied investment, reflecting fairness/reciprocity.
- Choices deviated from SPNE due to social preferences and trust considerations.

## LLM Session
- One-round Trust Game, multiplier = 3.
- LLM plays as either Player A or Player B.
- Prompts explicitly state role, multiplier, and available actions.
- Observations:
  - Early rounds: LLM sometimes returns part of investment (50%) to simulate fairness.
  - Later rounds: LLM converges to payoff-maximizing choice (return 0), reflecting rational expectation.
  - LLM behavior sensitive to prompt framing and payoff visibility.

## Comparative Analysis
- **Equilibrium prediction (SPNE):** Player A invests 0, Player B returns 0.
- **Human session:** Positive investments and partial returns, due to trust/fairness.
- **LLM session:** Mixture of fairness-oriented and payoff-maximizing behavior.
- Proposed refinement: *Behavioral SPNE* — replaces material payoffs with social-preference utilities and allows probabilistic choices (quantal response).

## References
- Camerer, C. F. (2003). *Behavioral Game Theory: Experiments in Strategic Interaction*. Princeton University Press.
- NashPy documentation: <https://nashpy.readthedocs.io/>
- oTree: <https://otree.org/>
- Shoham, Y., & Leyton-Brown, K. (2009). *Multiagent Systems: Algorithmic, Game-Theoretic, and Logical Foundations*. Cambridge University Press.
