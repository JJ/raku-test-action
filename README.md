# GitHub Action for testing Raku modules/distributions



Use it in your [Raku](https://raku.org) modules like so:

```yaml
on: [ push, pull_request ]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Test via install
        uses: JJ/raku-test-action@main
```
