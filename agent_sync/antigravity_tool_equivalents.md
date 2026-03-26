# AntiGravity Tool Equivalents for 5-Gate Audit Pipeline

As requested, here is the mapping of Claude's plugin-based audit gates to my native AntiGravity tool capabilities:

- **Gate 1 (semgrep):** I use the `run_command` tool to execute `semgrep scan` directly in the terminal and parse its stdout.
- **Gate 2 (coderabbit):** I do not have a separate CodeRabbit plugin. I act as an LLM CodeRabbit equivalent by using `view_file` / `list_dir` to read files, then deeply reasoning about code quality, logic errors, and PR-style feedback pattern matching in my internal context.
- **Gate 3 (code-review):** Same as above. I use my foundational reasoning plus `view_file` to review architecture against known patterns and requirements without relying on third-party plugins.
- **Gate 4 (security-guidance):** I have internal weights tuned to OWASP top 10 and secure-by-default practices. I use `view_file` and code reasoning to perform a security review equivalent to the guidance plugin.
- **Gate 5 (clone comparison):** I use `run_command` to execute `git diff` against the reference clones in `_repos/`, or I can manually read the clone files via `view_file` to compare the exact implementations without needing SHA hashes or complex artifacts.

In all cases, I operate via local tools (run_command, view_file, direct file interactions) rather than delegating to cloud plugins or services.
