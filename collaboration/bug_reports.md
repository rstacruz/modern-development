# Submitting bug reports

Here are some guidelines when filing bug reports for your tool of choice.

## Titles

**Keep the title short.**
Put any details in the body, not in the title. This makes it easier to digest a long list of issues.

> - "When I try to change passwords, an error is raised." <em class='bad-example'>*...can be shorter*</em>
> - "Can't change passwords" <em class='good-example'>OK!</em>

**Don't be too general.** Try to be more specific when possible.

> - "Products error"  <em class='bad-example'>*...too broad*</em>
> - "Can't buy products" <em class='bad-example'>*...still too broad*</em>
> - "Product page error" <em class='bad-example'>*...still too broad*</em>
> - "Product page: the buy button isn't clickable" <em class='good-example'>OK!</em>

## Details

> <h4 class='quote-heading'>Bug report example</h4>
>
> ## Can't change passwords
> When I'm logged into as a User, the "change email" form returns an error. Using Firefox on OSX.
  
**Write a short description.** Add a one-sentence (or one-paragraph) in the body of the issue.

**Be detailed.** For bug reports, make sure that the following details are available or are obvious:

  * URL *(if applicable)*
  * Environment *(OS, browser, website environment)*
  * Steps to reproduce
  * Expected result
  * Actual result
  
**But not too detailed.** You don't need to actually list *all* of them (especially for simple issues), just make sure that anyone can figure those details out.

**Be visual.** Include screenshots when possible!

## Short example

There's no need to include steps, expected result, and actual result when it's obvious.

> <h4 class='quote-heading'>Bug report example</h4>
>
> ## Avatars are not shown

> The user directory is missing avatars. (OS X, Firefox, Production)<br>
> http://oursite.com/users
>
> ![Screenshot](https://placehold.it/150x100/fff/eee)

## Full example

> <h4 class='quote-heading'>Bug report example</h4>
>
> ## Can't send email
>
> The "send email" button isn't clickable.
> Using Firefox/OSX on Production.<br>
> See: http://oursite.com/user/23/edit
>
> ![Screenshot](https://placehold.it/150x100/fff/eee)
>
> 1. Log in as a user
> 2. Go to the Inbox page
> 3. Click "write new email"
> 4. Click "send"
>
> Expected: The email will be sent.<br>
> Actual: A JavaScript error appears when "send" is clicked.

&nbsp;

> **Next:** [...](../toc/README.md)
