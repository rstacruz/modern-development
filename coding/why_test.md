# Why we test

Writing tests make you work faster. This seems like a backward thought at first, since writing tests take time. In practice, these tests are automating parts of your workflow, and automation always makes you faster in the long run.

## F5-driven development

Let's consider the alternative to TDD. Development in the console usually involves a REPL shell that lets you invoke some code in your project. Here's an example in a typical Rails project:

```bash
$ bundle exec rails console
Loading development environment (Rails 5.0.0.1)

irb> User.new(first_name: 'John', last_name: 'Smith').full_name
"John Smith"
```

People often abuse REPL consoles as part of their coding process. A common anti-pattern is to use a REPL to test changes as you make them. A typical REPL workflow looks like this:

* Make some more changes.
* Press <kbd>Alt</kbd><kbd>Tab</kbd> to switch to a terminal.
* Press <kbd>Up</kbd> then <kbd>Enter</kbd> to retry the last command.

In the case of web development, switching to a browser and hitting <kbd>Ctrl</kbd><kbd>R</kbd> or <kbd>F5</kbd> to reload is also very common. Wouldn't it be easier to automate this process for you?

```rb
test 'Builds a full name do' do
  user = User.new(
    first_name: 'John',
    last_name: 'Smith')

  expect(user.full_name).to eq 'John Smith'
end
```

By writing those same REPL commands as a test, you can now re-run it using `ruby test/user_test.rb`. In fact, you can run all the tests you've ever written!

## Tests as insurance

Tests let you update code mercilessly. Have you ever been in a project that uses very old versions of 3rd-party libraries such as Rails or jQuery? These projects are too afraid to upgrade knowing it may break things.

By writing tests, you'll be alerted of breakages when updating your project's dependencies. Changing the jQuery version may make some tests fail. You'd know then where to fix things.

## Refactoring mercilessly

Tests aren't only for upgrading 3rd-party dependencies. Even updating one part in your project can result in breaking another part. A good refactoring process starts with writing tests. When changing code, it helps to know what it can break.

## Tests as documentation

While tests are no substitute for formal documentation, it can provide a quick reference for other developers. Consider this test:

```js
test('OrderCalculator calculating charges', t => {
  let order = {
    type: 'pickup', // or 'deliver'
    items: [
      { product: 'Glazed donut', price: 2.99, qty: 2 },
      { product: 'Coffee', price: 3.99, qty: 1 } ] }

  let charges = OrderCalculator.getCharges(order)
  t.deepEqual(changes, {
    subtotal: 9.97,
    tax: 1.19,
    delivery: 0,
    total: 11.16 })

  t.end()
})
```

Another developer would easily know at a glance what `OrderCalculator` does, what input it takes, and what results it yields.

> **Next:** Enforce code style guidelines through [linting](linting.md).
