# Writing bug reports

> <h4 class='quote-heading'>Bug report example</h4>
>
> ## Can't change passwords
> When I'm logged into as a User, the "change email" form returns an error. Using Firefox on OSX. See `oursite.com/users/23/edit`.
>
> ![Screenshot](https://placehold.it/300x100/fff/eee)

A good bug report has a short title, a one-sentence short description, relevant details, and screenshots. Make sure these details are listed down, or are obvious enough:

  - URL <em class='bad-example'>(if applicable)</em>
  - Environment <em class='bad-example'>(OS, browser, website environment)</em>
  - Screenshot
  - Steps to reproduce
  - Expected result
  - Actual result

## Writing titles

Keep the title short. Put any details in the body, not in the title. This makes it easier to digest a long list of issues.

> - "When I try to change passwords, an error is raised." <em class='bad-example'>*...can be shorter*</em>
> - "Can't change passwords" <em class='good-example'>OK!</em>

Try to be specific. Titles that are too broad are not helpful.

> - "Products error"  <em class='bad-example'>*...too broad*</em>
> - "Can't buy products" <em class='bad-example'>*...still too broad*</em>
> - "Product page error" <em class='bad-example'>*...still too broad*</em>
> - "Product page: the buy button isn't clickable" <em class='good-example'>OK!</em>

## Full example

This example also includes steps, actual result, and expected result details. While some reports don't need all these details, it's a good idea to include them anyway.

> <h4 class='quote-heading'>Bug report example</h4>
>
> ## Can't send email
>
> The "send email" button isn't clickable.
> Using Firefox/OSX on Production. See `oursite.com/user/23/edit`.
>
> ![Screenshot](https://placehold.it/300x100/fff/eee)
>
> #### Steps
>
> 1. Log in as a user
> 2. Go to the Inbox page
> 3. Click "write new email"
> 4. Click "send"
>
> Expected: The email will be sent.<br>
> Actual: A JavaScript error appears when "send" is clicked.

_

> **Next:** [...](../toc/README.md)
