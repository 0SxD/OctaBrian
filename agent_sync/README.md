# agent_sync/ — Blackboard Protocol (Stage 1 of Dual-Stage Airlock)

## Purpose

Coordination layer for ALL agents: Claude Code sub-agents + Gemini AntiGravity.
This is Stage 1 of the airlock. ALL agent output is audited here before any git operations.

## Participants

| Agent | Role | Writes requests? | Writes results? |
|---|---|---|---|
| Claude (Opus) | Orchestrator | Yes | No (writes summaries only) |
| Claude (Sonnet) | Audit gate agent | No | Yes |
| Gemini (AntiGravity) | Code writer + audit partner | No | Yes |
| Codex | Code writer | No | No (audited by Claude pipeline) |

## File Contract — audit_request_{id}.md

```yaml
---
request_id: {timestamp-based, e.g. 20260325-143022}
status: pending | in_progress | pass | fail
requestor: opus-orchestrator
target_files:
  - path/to/file.py
what_to_check: [description]
pass_criteria: [specific conditions for PASS]
fail_criteria: [specific conditions for FAIL]
audit_gates:
  - semgrep
  - coderabbit
  - code-review
  - security-guidance
  - clone-repo-comparison
---
```

## File Contract — audit_result_{id}_{gate}.md

```yaml
---
request_id: {matches request}
status: pass | fail
auditor: sonnet-agent | gemini-antigravity
gate: semgrep | coderabbit | code-review | security-guidance | clone-repo-comparison
findings: [list or "none"]
verdict: PASS | FAIL
issues:
  - [specific file:line if FAIL]
timestamp: ISO8601
---
```

## File Contract — audit_summary_{id}.md

Written by Opus after all gates complete:

```yaml
---
request_id: {matches request}
stage1_verdict: PASS | FAIL
gates:
  semgrep: PASS | FAIL
  coderabbit: PASS | FAIL
  code_review: PASS | FAIL
  security_guidance: PASS | FAIL
  clone-repo-comparison: PASS | FAIL
blocking_issues: [list if any FAIL]
austin_approved_exceptions: [list if any]
ready_for_stage2: true | false
---
```

## Audit Loop Protocol

1. Execute → Audit → FAIL → Fix → Re-audit
2. If same issue recurs: STOP. Research why. Different approach.
3. Max 2 re-audits per gate before escalating to Austin.
4. A fix without a passing re-audit is NOT a pass.
5. Both executor AND auditor must pass for work to be considered done.

## Rules

- NO SARIF files. NO SHA hashing. NO crypto tags.
- Audit trail = git history + comparing against clone repos in _repos/
- Status transitions: pending → in_progress → pass/fail
- Completed files stay as history — do not delete
- Any agent (Claude sub-agent or Gemini) can write result files
- Only Opus creates request files
- Each gate = separate agent with clean context (zero-context reviewer pattern)
- Exception: Gemini AntiGravity (IDE-embedded) may run multiple gates in one pass but MUST write separate audit_result files per gate.
- On ANY violation: Opus asks Austin. Agents do NOT decide exceptions.
- NO custom code without Austin's explicit permission. If a library exists, use it.
- All GitHub repos PRIVATE unless Austin explicitly approves public.
