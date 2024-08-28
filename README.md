A GitHub Action to filter comments for suspicious content.

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
      uses: DecimalTurn/Comment-Filter@5ab6948d08be719961eac47fad2b2a91a06fc4c9 #v0.1.0
```
## FAQ

### Is the action fast enough to alter the content of the notification email?

Yes, normally the action will be fast enough to change the content of the comment before it gets picked up by the GitHub background job in charge of sending the email notification ([Demo](https://github.com/DecimalTurn/Comment-Filter-Demo/issues/1#issuecomment-2315663776)).
