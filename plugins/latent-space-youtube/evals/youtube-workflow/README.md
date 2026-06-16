# YouTube Workflow Review Evals

These scenarios help maintainers review whether the plugin still follows the
intended Zoom-to-YouTube workflow before publishing a new version.

Run a case in Claude Cowork, Claude Code, Codex, or another agent harness, save
the agent's response, and score it with `rubric.md`. The goal is human-in-the-loop
workflow review: checkpoints, duplicate detection, user confirmation, and safe
handling of publishing/deletion steps matter more than fully automated pass/fail.

These cases can later be connected to Telvine eval runs alongside production
metadata such as skill invocations, errors, and user feedback.
