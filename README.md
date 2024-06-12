

- print all outputs as json:
```yaml
    steps:
      # need id to reference the step
      - id: release_please
      - run: |
          echo '${{ toJSON(steps.release_please.outputs) }}'
```

- set outputs:
```yaml
jobs:
  
  job1:
    outputs:
      key: ${{ steps.step1.outputs.key }}
      
    steps:
        - id: step1
        - run: |
            echo "key=value" >> $GITHUB_OUTPUT
```
