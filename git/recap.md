# Recap

- Everything you do has to be reviewed by someone else.
- It should be easy to review other people's work.
- All work happens in feature branches and have pull requests.
- Nobody should ever commit directly into `develop` or `master`.

#### The main branches

- `develop` is always ready for developers and testers.
- `master` is always ready for users.

#### Making changes

- Create a feature branch.
- Send a pull request for this feature branch into `develop`.
- Your team will need to review and merge this pull request.

#### Releasing versions

- Merge `develop` into `master`.
- Create a GitHub release.

#### Deploying emergency hotfixes

- Create a branch from `master`.
- Send a pull request for this branch into `master`.
- Merge `master` back to `develop` if necessary.

## See also

This git workflow is based on [git-flow].

- [git-flow]() (nvie.com)
- [GitLab flow](https://about.gitlab.com/2014/09/29/gitlab-flow/) (gitlab.com)
- [Git manual]() (git-scm.com)

[git-flow]: http://nvie.com/posts/a-successful-git-branching-model/
[Git manual]: https://git-scm.com/documentation
