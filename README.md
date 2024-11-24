# Get issue labels action

This action get issue labels via gh client

## Usage

Here's an example of how to use this action in a workflow file:

```yaml
name: Example Workflow
jobs:
  lint:
    name: Lint
    runs-on: ubuntu-latest
    permissions:
      issues: write
    steps:
      - name: Add Label
        uses: rubycats-com/issue-add-label-action
        with:
          number: ${{ github.event.issue.number }}
          label: 'delivered'
```

## Inputs

| Input    | Required | Description |
|----------|----------|-------------|
| `number` | true     | Issue id    |
| `label`  | true     | Label title |

Please make sure that label with this title is available

## Outputs

No outputs in this action
