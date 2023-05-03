# GitHub Action to install Buck2

[<img alt="build status" src="https://img.shields.io/github/actions/workflow/status/dtolnay/install-buck2/ci.yml?branch=latest&style=for-the-badge" height="20">](https://github.com/dtolnay/install-buck2/actions?query=branch%3Alatest)

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
