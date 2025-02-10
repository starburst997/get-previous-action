# get-previous-action
Get the previous run's sha for Github Action

## Usage:

```yml
- name: Get the url of a diff between this commit and the one from the previous run
  uses: starburst997/get-previous-action@v1
  with:
    token: ${{ secrets.GH_PAT }}
```