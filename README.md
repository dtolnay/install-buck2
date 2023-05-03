# GitHub Action to install Buck2

This GitHub Action installs a precompiled `buck2` binary from
<https://github.com/facebook/buck2/releases/tag/latest>.

```yaml
name: test suite
on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: dtolnay/install-buck2@latest
      - run: buck2 build //...
```
