## GitHub Actions Workflow

A **workflow** defines an automated process that runs in response to specific events in a GitHub repository. Each workflow specifies:

- **When** it runs — the triggering event (e.g., `push`, `pull_request`)
- **Where** it runs — the execution environment (e.g., `ubuntu-latest`)
- **What** it does — the commands(steps) or actions to be executed

### Workflow Structure

- A workflow consists of one or more **jobs**.
- Each **job** is made up of a sequence of **steps**.
- **Steps** within a job run **sequentially**.
- **Jobs** can run **in parallel** by default or **sequentially** when dependencies are defined using `needs`.

This structure allows workflows to be modular, parallelizable, and easy to maintain.

Events are GitHub activities that trigger workflows:

- `push` - Someone pushes code
- `pull_request` - Someone opens/updates a PR
- `schedule`  - Time-based (cron)
- `workflow_dispatch` - Manual trigger (click button in UI)
-  `release` - Someone creates a release
- `issues` - Issue created/opened
- Custom: `repository_dispatch`(webhook)

You can filter triggers (only on certain branches, paths, etc.)
##  Branch-specific Triggers 
`.github/workflows/branch-filter.yml`