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
      uses: DecimalTurn/Comment-Filter@main
```
By using the version from the `main` branch, you make sure to always have the most up-to-date rules for the filter.


## FAQ

### Is the action fast enough to alter the content of the notification email?

Yes, normally the action will be fast enough to change the content of the comment before it gets picked up by the GitHub background job in charge of sending the email notification ([Demo](https://github.com/DecimalTurn/Comment-Filter-Demo/issues/1#issuecomment-2315663776)).

## Contributing

Contributions to this project (such as pull requests, bug reports, etc.) are welcomed! :octocat:
If you do, please make your PR against the `dev` branch.
