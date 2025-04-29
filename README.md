# nuclei-templates

## Nuclei favicon-detect additions

```yaml
- type: dsl
  name: "iqmessenger"
  dsl:
    - "status_code==200 && (\"1033082340\" == mmh3(base64_py(body)))"

- type: dsl
  name: "topdesk"
  dsl:
    - "status_code==200 && (\"-1177777311\" == mmh3(base64_py(body)))"

- type: dsl
  name: "schneider-electric"
  dsl:
    - "status_code==200 && (\"-139383140\" == mmh3(base64_py(body)))"

- type: dsl
  name: "usergate"
  dsl:
    - "status_code==200 && (\"-782553370\" == mmh3(base64_py(body)))"

- type: dsl
  name: "sonatype-nexus-repository-manager"
  dsl:
    - "status_code==200 && (\"1323738809\" == mmh3(base64_py(body)))"
```
