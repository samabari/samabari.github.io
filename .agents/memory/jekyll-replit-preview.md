---
name: Jekyll preview on Replit
description: Avoid repeated Jekyll rebuilds caused by Replit's workflow logs.
---

When running Jekyll with its file watcher in this Replit workspace, exclude `.local` from the site source. Also exclude `.agents`, `.cache`, and `.config` so workspace metadata and generated files do not become site output.

**Why:** Replit writes workflow logs under `.local/state/workflow-logs`; Jekyll's watcher treated log updates as source changes and repeatedly regenerated the site. A stopped temporary server can also leave a stale `[[ports]]` mapping to external port 80, causing the project domain to return 502.

**How to apply:** Keep these workspace directories in Jekyll's `exclude` list, bind the preview server to `0.0.0.0` on the configured workflow port, and map that port to external port 80. Remove temporary server mappings before finishing.
