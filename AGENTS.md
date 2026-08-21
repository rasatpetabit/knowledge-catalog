# AGENTS.md — knowledge-catalog

Knowledge catalog / OKF-related catalog work.

<!-- agentic-dispatch:central-pointer v2 -->
## Central agent policy

Cross-repo AskUserQuestion/ask_user_question (AUQ), Serena, Hindsight,
context-mode, and subagent/model-dispatch policy is centralized in the
agent-dispatch repo. Read it via `agent-dispatch where` (repo root) or
`agent-dispatch digest` (live routing policy). Do not duplicate or override
that policy here.

<!-- agent-dispatch:begin routing hash=ab9bc373a67846a9f7ca9d9e4cff415f061bf461e385ef3020963d0799821040 -->
## §routing — managed by agent-dispatch (do not hand-edit)

Binding rules (enforced by PreToolUse guard):
- Some models are gated and require a live override grant; run `agent-dispatch digest` for current dispositions.
- model param MUST be explicit — missing model is denied, EXCEPT the built-in read-only types below (Explore/Plan), which inherit the session model.
- Route work to the roster role its class names (routing.yaml classes[].agent); the role pins the lane. Explore/Plan are exempt built-ins that BYPASS lane routing: dispatch them WITHOUT a model param (they inherit the session model; an explicit model outside the lineup is denied). Prefer the role.

For the full routing policy, fallback chains, and backend health:
  agent-dispatch digest          # live, from the canonical policy file
  agent-dispatch resolve <class> # deterministic tier for a task class

Source of truth: policy/dispatch-policy.jsonc in the agent-dispatch repo (run `agent-dispatch where` for its root).
<!-- agent-dispatch:end -->
