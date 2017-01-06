# Reviewing pull requests

A pull request reviewer has these responsibilities:

- Understand the original author's changes so that the knowledge is shared across the team.
- Find any issues the changes may have.

A reviewer should do one of these things:

- Approve it (by merging the pull request);
- Reject it (by request for changes); or
- Ask others to review it as well (by saying "LGTM").

## Who can review

Anyone on the team can review anyone else's code. Senior members typically do most the reviews in practice, but any member of the team can review pull requests as long as they can satisfy the responsibilities listed above.

The only person who can't review the code is the original author.

As a pull request reviewer, you will be partly responsible for the pull request's code.

## Understanding the pull request

A review will be partly responsible for the code's presence in the project. Should anyone have concerns about it in the future, it's going to be the author and the reviewer who should be able to answer these concerns.

A reviewer should also test the pull request, if possible.

## Approving

Simple. Merge the pull request to approve it!

If you'd like to offer your review but don't want to merge it yourself, you can leave a comment saying "LGTM." This can either mean "looks good to me" or "let's get this merged." This is useful if you'd rather wait for the input of another colleague.

## Rejecting

A reviewer may request for changes as a way of rejecting a pull request.

- Use GitHub's "request changes" facility to request for changes.
- Remove the `For review` tag in the pull request.

When the author's done the changes, it should be tagged back as `For review`.

<details>
<summary>See also...</summary>

<ul>
<li><a href='https://help.github.com/articles/reviewing-proposed-changes-in-a-pull-request/'>Reviewing proposed changes in a pull request</a> (github.com)</li>
<li><a href='https://help.github.com/articles/about-pull-request-reviews/'>About pull request reviews</a> (github.com)</li>
</ul>
</details>

> **Next**: [Building a release](releasing.md)
