---
icon: bug
---

# Test, debug, and inspect runs

Run a workflow with safe input before relying on it. Check what triggered it, which parameters reached each step, and which records changed.

1. Try a normal case, an empty result, and a failure path.
2. Inspect outputs and error actions. Confirm retries or duplicate events will not create unintended changes.
3. Test a user or service credential with the permissions the workflow will use in production.
4. Record the failed step and input when troubleshooting.

Follow [Test & Debug](test-and-debug.md) for the editor controls. If the workflow invokes an agent, also [test that agent](https://app.gitbook.com/s/-LQ08RFAKZvFADEiXKFy/ai-agents) against its allowed tools.
