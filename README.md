# get-previous-action
Get the previous run's sha for Github Action

My use case was to show the URL to compare the commits between two successful run (manual) 

## Usage:

```yml
- name: Get the url of a diff between this commit and the one from the previous run
  id: previous
  uses: starburst997/get-previous-action@v1
  with:
    token: ${{ secrets.GH_PAT }}
- run: |
    echo Previous SHA: ${{ steps.previous.outputs.sha }}
    echo Diff url: ${{ steps.previous.outputs.diff-url }}
```