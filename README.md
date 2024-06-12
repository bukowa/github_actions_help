

- print all outputs as json:
```yaml
    steps:
      - uses: ...
        # need id to reference the step
        id: release_please

      - name: ...
        run: |
          echo '${{ toJSON(steps.release_please.outputs) }}'
```