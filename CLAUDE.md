# Cairn

Open-source DORA metrics for engineering teams, an alternative to DX. A hosted GitHub App built with TypeScript (Next.js, Postgres). It starts with DORA and later grows into arbitrary custom metrics.

The project is at an early stage and has no code yet. The plan lives in GitHub Issues, starting at the root issue #1.

## Use GitHub's native features

Always make best use of GitHub's own features instead of keeping the same information in files or other tools.

- **Issues** describe features, bugs, tasks, decisions and research questions. Start work from an issue, and reference it in commits and pull requests (`Closes #N`). If there isn't an issue for the work, create one first.
- **Sub-issues** hold the hierarchy: root #1, then the milestone epics M0 to M5, then tasks. Add new work as a sub-issue of the relevant epic, and use a nested sub-issue only where a task has parts that are tracked separately. `gh issue` has no sub-issue command, so link with the API: get the child's database id with `gh api repos/baggerspion/cairn-metrics/issues/<n> --jq .id`, then `gh api -X POST repos/baggerspion/cairn-metrics/issues/<parent>/sub_issues -F sub_issue_id=<id>`.
- **Labels** give each issue one type (`epic`, `research`, `enhancement` or `bug`) and at most one area (`backend`, `frontend`, `infra`, `metrics` or `launch`).
- **The wiki** holds documentation and research findings, such as competitor analysis, decisions and how-tos. Don't commit that kind of material as markdown in the repo. Keep in the repo only what GitHub or the code needs: `README.md`, `LICENSE`, `CLAUDE.md` and files such as `CONTRIBUTING.md`.
- **Pull requests** carry code changes and link the issue they resolve.

If a native GitHub feature fits, use it. If you are unsure which one to use, ask.

## Notes

- The repo is public. Issues, pull requests and the wiki are visible to everyone, so never put secrets, personal details or customer data in them.
- The GitHub account is `baggerspion`, and `origin` uses the `github.com-personal` SSH alias. Check `gh auth status` shows `baggerspion` as the active account before using `gh`.
- Cairn is its own first user. Once the GitHub App exists it is installed on this repo, which is why the repo moves to PR-only changes to `main` (issue #17).
