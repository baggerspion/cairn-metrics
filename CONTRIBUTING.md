# Contributing to Tuig

Thanks for your interest. Tuig is early, so the best contributions right now are bug reports, ideas and feedback.

## Licence

Tuig is licensed under the [GNU Affero General Public License v3.0](LICENSE). By contributing, you agree that your contribution is licensed under the same terms.

## Sign off your commits (DCO)

Tuig uses the [Developer Certificate of Origin](https://developercertificate.org/) instead of a contributor licence agreement. You keep the copyright in your contributions. To certify the DCO, add a sign-off line to every commit:

```
git commit -s -m "Your message"
```

This adds `Signed-off-by: Your Name <you@example.com>`, which must match the commit author.

A GitHub Action checks every pull request and fails if any non-merge commit lacks a matching sign-off. To fix it, run `git commit --amend -s --no-edit` for the last commit, or `git rebase --signoff <base>` for several, then `git push --force-with-lease`. Commits made in GitHub's web editor are signed off automatically.

Commits to `main` must also carry a verified signature (GPG, SSH or S/MIME). That is separate from the DCO sign-off, and GitHub rejects unsigned commits.

## How to contribute

1. **Start with an issue.** Look at the [open issues](https://github.com/tuighq/tuig/issues) or open a new one to describe the bug or feature. Larger changes are best discussed first.
2. **Open a pull request** that links the issue (`Closes #N`) and keeps to one logical change.
3. **Documentation and research notes** go in the [wiki](https://github.com/tuighq/tuig/wiki), not in the repository.
