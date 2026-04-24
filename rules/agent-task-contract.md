# Agent Task Contract

All non-trivial agent tasks in this repository must declare the same operating contract before execution.

## Required Sections

1. `Objective`
2. `Inputs`
3. `Write Scope`
4. `Constraints`
5. `Output Contract`
6. `Verification`
7. `Recovery`

## Rules

- Builders do not self-certify high-impact output.
- Validators are read-only unless the workflow explicitly grants revise authority.
- If the same failure class occurs twice, switch strategy instead of repeating the same retry.
- Use worktree isolation for bounded parallel tasks where comparison creates value.
- Risky automation must run in sandbox first.
- Every workflow run should emit a run manifest with task, agent, files touched, retries, and outcome.

## Failure Classes

Use one of these values when logging or routing failures:

- `schema_failure`
- `factual_failure`
- `brand_failure`
- `quality_failure`
- `state_failure`
- `integration_failure`
- `unsafe_operation`
- `unknown_failure`
