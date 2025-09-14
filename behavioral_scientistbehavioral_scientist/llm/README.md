## LLM Session

- **Game setup:** One-round Trust Game, multiplier = 3.  
- **Roles:** LLM plays as either Player A or Player B depending on the round.  
- **Prompt template example (for Player B):**
- You are Player B in a one-round Trust Game.
Player A invested X.
Multiplier is 3.
Choose how much to return to Player A (0, 50%, or 100%) and explain your reasoning.

### Session Summary
| Round | Player A Investment | Player B Return | Player A Payoff | Player B Payoff |
|-------|-------------------|----------------|----------------|----------------|
| 1     | 50                | 75             | 125            | 75             |
| 2     | 0                 | 0              | 100            | 0              |
| 3     | 50 (LLM as A)     | 0              | 50             | 150            |
| 4     | 100 (LLM as A)    | 0              | 0              | 300            |
| 5     | 0 (LLM as A)      | 0              | 100            | 0              |

### Observations
- LLM’s behavior combines rational and fairness-oriented patterns.  
- When acting as Player B:
- Early rounds: sometimes returns 50% of investment to encourage trust.  
- Later rounds: converges to payoff-maximizing choice of 0.  
- When acting as Player A: anticipates B’s strategy and adjusts investment accordingly.  
- Behavior shows sensitivity to **prompt framing** and **payoff visibility**.  

### Files in `llm/`
- `prompts.txt` — all exact prompts used.  
- `transcript.md` — full session transcript with reasoning.  
- `settings.json` — LLM model, temperature, and other configurations.


