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
      uses: DecimalTurn/Comment-Filter@7cc4cabf18263951bfa9a5352fda002a090bd3f9 #v0.1.0
```
