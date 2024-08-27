# comment-filter
GitHub Action to filter comment for suspicious content.

Example worflow:

`Path: /.github/workflows/comment-filter.yml`

```yaml
name: Check for Spammy Issue Comments

on:
  issue_comment:
    types: [created, edited]

permissions:
  issues: write

jobs:
  comment-filter:
    runs-on: ubuntu-latest
    steps:
    - name: Comment filter
      uses: DecimalTurn/Comment-Filter@main
```