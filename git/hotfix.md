# Emergency fixes

There are times when bug fixes must be made outside the release cycle. This is called a *hotfix*.

The main branches (`develop` and `master`) are never to be pushed directly to, and hotfixes are no excuse to violate this rule. Instead, they should be made as hotfix branches.

## Hotfix branches

Hotfixes branches are just like feature branches. They're worked on in the same way: pull requests, review, merge. The only difference is that they're branched from `master` instead of `develop`.

```sh
# Switch to the master branch
git checkout master

# Create your branch
git branch hotfix/security-fix

# Start working!
```

## Merging hotfixes

Pull requests are made for hotfixes too, just like feature branches. A colleague will have to review and merge your pull request, ideally.

The `master` branch will be updated once a pull request is merged in. This should trigger your automated deployment process and deploy the hotfix to production servers.

## Syncing the develop branch

Once the pull request is merged, `master` now has the fixes, but not `develop`. In these cases, you can do one of two things:

- Option A: Merge `master` back into `develop`.
- Option B: Merge the hotfix into `develop` as well ("backporting").

Option A is preferred in most cases, with option B only being used when merging `master` back may be too complicated.

## Self-merging

There may be cases when fixes are time-sensitive and colleagues aren't available to review and merge your changes. If this happens:

- Create a pull request as usual.
- Merge the pull request yourself.
- Leave a comment in the pull request with the reason for urgency.
- Inform your teammates afterwards so they can still review your changes.

<details>
<summary><em>See also...</em></summary>

<ul>
<li><a href='https://en.wikipedia.org/wiki/Backporting'>Backporting</a> (wikipedia.org)
</ul>
</details>

> **Next:** [Why we use branches](why.md)
