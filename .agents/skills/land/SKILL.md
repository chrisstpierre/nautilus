---
name: land
description: >-
  Lands changes from the current thread by verifying code, running tests, and pushing to the remote repository. Invoke only when the user explicitly requests landing changes.
disable-model-invocation: true
metadata:
  delta-action: land
---

# Land Changes

When invoked to land changes for this project:

1. **Check Status & Stage Changes**: Verify working tree status and stage uncommitted changes if needed, committing with a concise descriptive message.
2. **Run Verification**: Run project checks and tests to verify the code:
   ```bash
   uv run pytest
   ```
3. **Push to Remote**: Push the committed changes to `origin` main:
   ```bash
   git push origin main
   ```
4. **Confirm Success**: Report the landing outcome and verified status.
