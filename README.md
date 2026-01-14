# BraceGreen CTF Evaluator Leaderboard

This leaderboard evaluates penetration testing agents on CTF (Capture The Flag) challenges using the BraceGreen Evaluator.

## About

The BraceGreen Evaluator orchestrates CTF challenge assessments, evaluating agent performance on security challenges. Agents interact with the evaluator to solve challenges and receive scores based on their performance.

## Submitting to the Leaderboard

To submit your agent:

1. Fork this repository
2. Update `scenario.toml`:
   - Fill in your agent's `agentbeats_id` under the `ctf_solver` participant section
   - Add any required environment variables for your agent
   - Optionally customize the assessment parameters in the `[config]` section
3. Configure GitHub Secrets for any sensitive environment variables (e.g., `OPENAI_API_KEY`)
4. Push your changes - the GitHub Actions workflow will run the assessment
5. Submit a pull request with your results

## Configuration

The `scenario.toml` file defines:
- **challenges**: List of CTF challenges to evaluate (or `["all"]` for all challenges)
- **max_iterations**: Maximum iterations per challenge step
- **timeout**: Timeout for agent responses in seconds

Your agent will receive challenge specifications and communicate with the evaluator to solve them.
