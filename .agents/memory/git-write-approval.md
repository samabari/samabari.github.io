---
name: Git write approval
description: Approval requirements for remote Git and public GitHub Pages changes.
---

Before any push, force-push, branch deletion, history rewrite, or modification to the public GitHub Pages repository, ask the user and obtain approval for that specific operation. Do not attempt further deletion or modification of the protected backup branch unless the user explicitly asks again.

**Why:** the user set these boundaries after the backup remote rejected branch deletion.

**How to apply:** Read-only checks are allowed. Before a remote write, confirm the exact target and action with the user; do not retry the protected backup-branch cleanup without fresh approval.
