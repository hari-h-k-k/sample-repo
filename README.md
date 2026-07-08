# aider-sample

A sample repo demonstrating [aider-bot](../aider-bot) in action.

## What's here

- `calculator.py` — a simple Python module with some rough edges (no error handling, manual loop instead of `*`, etc.)
- `.github/workflows/fix-review.yml` — the workflow that auto-fixes PR review comments using aider

## Try it out

1. Fork or push this repo to GitHub.
2. Add `OPENAI_API_KEY` to **Settings → Secrets and variables → Actions**.
3. Update the action reference in `.github/workflows/fix-review.yml`:
   ```yaml
   - uses: your-org/aider-bot@main
   ```
4. Open a PR that modifies `calculator.py`.
5. Leave an inline review comment like:
   - `divide` should raise a `ValueError` when `b` is 0
   - `multiply` should use `a * b` instead of a loop
6. Submit the review with **Request changes**.
7. Watch the action run and push the fixes automatically.
