# GitHub Action for testing Raku modules/distributions

> [Available from Github Action marketplace](https://github.com/marketplace/actions/raku-test-action)

Use it in your [Raku](https://raku.org) modules like so:

```yaml
on: [ push, pull_request ]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Test via install
        uses: JJ/raku-test-action@v2
```

It will install dependencies, test, and then cache installation so you don't
have to do it again in the future. It's using the latest version of Raku,
whatever that is at the moment.

if you want to include coverage in the tests, use this:


```yaml
on: [ push, pull_request ]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Test + coverage
        with:
          coverage: true
        uses: JJ/raku-test-action@v2
```

You can also use the `@main` if you want to be on the bleeding edge, but it's
not totally stable.

## Version history

### `v2`

Addresses Github-own actions deprecation

### `v1`

Initial release
