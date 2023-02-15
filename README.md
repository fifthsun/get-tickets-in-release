# get-tickets-in-release v1

This action is for gathering Jira ticket information from the 
git log for a release. You must supply a Jira ticket prefix 
to match against.

When a release workflow is triggered we determine the current
and previous version tags and then generate a log stream of 
all the git refs between 'previous..current'. 

A list of space seperated tickets are provided in the output.

## Usage
```
    - name: get-tickets-in-release
      id: get-tickets-in-release
      uses: fifthsun/get-tickets-in-release@v1
      with:
        project: MEG
```

## Output
```
    ${{ steps.get-tickets-in-release.outputs.tickets }}
```
