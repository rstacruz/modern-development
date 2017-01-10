# Inline documentation

```rb
# Publishes an article. This sets the `published_at`
# timestamp and makes the article appear in the
# `Article.published` scope.
def publish!
  ...
end
```

In an ideal world, we should always describe our work with documentation. In practical scenarios, we have time constraints and some things may be more important.

## Should I write documentation?

* **Prioritize tests over documentation.** A strong test suite has more long-term benefits than documentation, and good tests can be a poor substitute for documentation as well.

* **Prioritize documenting reusable parts.** If you're writing code that a teammate it likely to need in the future, write some documentation for it.

* **Prioritize documenting classes/modules** over individual methods. Documenting evry method is time consuming. If you little time to write documentation, prioritize documenting whole classes.

## Example

Here's a very basic example of documentation that was written in haste. Despite missing actual words, a quick glance can help a new developer understand how this class works and how it's used.

```rb
# A blog post.
#
# == Scopes
#
#     Article.published
#     Article.drafts
#     Article.feature
#
# == Methods
#
#     @article.publish!
#     @article.feature!
#
# == Presenters
# Also see +ArticlePresenter+.
#
#     @article.presenter.body_html
#     @article.presenter.body_markdown
#
class Article < ActiveRecord::Base
  ...
end
```

<blockquote class='note-callout -info'>
Note: this section mostly applies to private projects. Different ettiquette applies to documentation in open source projects.
</blockquote>

> **Next:** Let's [recap what we've learned](summary.md).
