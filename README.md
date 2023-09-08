# Anchor Test action

Github action for running Anchor tests for programs on the Solana blockchain

### Example action

```yaml
name: Program Tests
on:
  push:
    branches:
      - main
  pull_request:
jobs:
  program-tests:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repo
        uses: actions/checkout@v2
      - name: Solana Anchor Test
        uses: dcaf-labs/anchor-test-action@main
        with:
          args: "" # add anchor test args, e.g. "--skip-lint"
          workspace_dir: "." # path to the anchor workspace, e.g. "./my_workspace"
```
