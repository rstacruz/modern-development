Why use branches?
=================

We've been describing a git workflow that relies heavily on branches. This isn't the only way to use Git, of course. In fact, the most obvious way to use Git is how the [Git manual] first tells us to: push all commits to a single `master` branch.

This is great for solo developers, but this model breaks down once you have two or more on the team.

### Changes aren't contiguous

```
    X - X - O - O - X - O                  X - X - X - O - O - O

    Working on a single branch             Working using feature branches
    (interleaved)                          (contiguous)
```

If two people are working on 2 features, their commits may end up being interleaved. That is, for features `X` and `O`, the commits for either feature may not show up next to each other. This makes reviewing changes more difficult.

### Changes can't be reverted

To revert a feature that spans multiple commits, all those commits have to be reverted individually.

```sh
# Single-branch workflow: reverting each commit individually
git revert 1a84c2b9
git revert 9bf3cb70
git revert 6b9c5cb4
git revert 215c3820
```

Git solves this by grouping multiple commits together into a single *merge commit.* This is what happens when a pull request is merged. This merge commit can then be reverted, and doing so will revert all commits that it groups together.

```sh
# Feature branch workflow: only one commit to revert
# (Assuming 75a6c2a0 is a merge commit)
git revert 75a6c2a0 -m 1
```

#### Reviewing is difficult

It becomes harder to review changes when they're not contiguous or grouped in any way.

The Git workflow described here is a logical evolution brought about by the problems above.

[Git manual]: https://git-scm.com/documentation
