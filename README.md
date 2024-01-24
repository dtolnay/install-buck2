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
      - run: buck build //...
```

## Inputs

<table>
<tr>
  <th>Name</th>
  <th>Description</th>
</tr>
<tr>
  <td><pre>prelude-submodule</pre></td>
  <td>
    Optional. Relative path at which to checkout the
    <a href="https://github.com/facebook/buck2-prelude">buck2-prelude</a>
    repo as a submodule at the correct commit matching the installed buck2
    executable.
  </td>
</tr>
</table>

## Outputs

<table>
<tr>
  <th>Name</th>
  <th>Description</th>
</tr>
<tr>
  <td><pre>prelude-hash</pre></td>
  <td>
    Commit hash of the
    <a href="https://github.com/facebook/buck2-prelude">buck2-prelude</a>
    repo that matches the installed buck2 executable.
  </td>
</tr>
</table>
