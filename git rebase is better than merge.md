---
tags: [git]
---

# [[Git]] Rebase is Better than Merge

https://www.atlassian.com/git/tutorials/merging-vs-rebasing#:~:text=Merging%20is%20a%20safe%20option,onto%20the%20tip%20of%20main%20.

Rebase can be a nice way to remove extraneous commits.

Rebase is a better alternative to merge for updating featurebranch with master’s new commits

Rebase should not be used on public branches. That includes:

- Branches with associated PRs
- Master branch

You should instead:

- Rebase _after_ the PR is approved

## Conclusion

Looks like rebase is useful on local branches, but probably shouldn’t be used during PR
