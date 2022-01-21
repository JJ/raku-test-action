# GitHub Action for testing Raku modules/distributions



Use it in your [Raku](https://raku.org) modules like so:

```yaml
on: [ push, pull_request ]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Test via install
        uses: JJ/raku-test-action@main
```

It will install dependencies, test, and then cache installation so you don't
have to do it again in the future. It's using the latest version of Raku,
whatever that is at the moment.
